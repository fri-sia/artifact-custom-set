
<template>
    <div :class="classes" v-bind:style="{ width: width + 'px' }">
        <img :height="height" :src="cardBg" alt="">
        <div class="top">
            <span v-if="color !== 'item'" class="manacost">{{manacost}}</span>
            <span class="name">{{name}}</span>
            <span v-if="color === 'item'" class="itemcost">{{cost}}</span>
        </div>
        <div class="cardtype-icon">
            <img :src="cardTypeIcon" alt="">
        </div>
        <div :style="bgImageStyle(bgImage, bgTopOffset)" class="bg-image" :data-bg="bgImage"></div>
        <div class="bg-desc"></div>
        <div class="desc-text">
            <slot name="description"></slot>
            <span class="tags">{{tags}}</span>
        </div>
        <div v-if="type === 'hero' || type === 'creep'" class="bottom">
            <span class="attack">{{attack}}</span>
            <span v-if="armor !== '0'" class="armor">{{armor}}</span>
            <span class="health">{{health}}</span>
        </div>
        <div class="detailed-information">
            <h3>{{name}}</h3>
            <div class="properties">
                <div class="property">Type</div>
                <div class="value">{{capitalize(type)}}</div>

                <div class="property">Color</div>
                <div class="value"><span :class="color">{{capitalize(color)}}</span></div>

                <div class="property">Manacost</div>
                <div class="value">{{manacost}}</div>
                
                <div class="property" v-if="type === 'improvement' && (crosslane !== false) || crosslane">Crosslane</div>
                <div class="value" v-if="type === 'improvement' && (crosslane !== false) || crosslane">Yes</div>

                <div class="property">Tags</div>
                <div class="value tags-value">{{tags}}</div>
            </div>
            <div class="detailed-information-desc-text">
                <slot name="description"></slot>
            </div>
            <div class="keywords-clarification">
                <template v-if="keywords.includes('Ascend')">
                    <h5>Ascend</h5>
                    <div class="keyword-description">
                        <p>If you have a unit with “Ascend {color}”, you may play cards of that color as if the unit was a hero.</p>
                        <p>Stuns, silences and other status effects limiting what cards you are able to play works the same way on ascended creeps as they do on heroes.</p>
                    </div>
                </template>
                <template v-if="keywords.includes('Transcend')">
                    <h5>Transcend</h5>
                    <div class="keyword-description">
                        <p>Transcend {color} gives an extra effect if you are able to play cards of the given color.</p>
                        <p><i>It is considered a card of the transcended color in addition to its other colors while the color requirement is met.</i></p>
                        <p><i>If found on a continuous effect, the effect lasts as long as the color requirement is met, updating on pulses.</i></p>
                    </div>
                </template>
                <template v-if="keywords.includes('Banish')">
                    <h5>Banish</h5>
                    <div class="keyword-description">
                        <p>Banished units are moved to a zone similiar to the fountain, except that they don't heal and modifications lasting “until the unit dies” are not removed.</p>
                        <p>Banished units do not automatically redeploy but do so by a card or ability effect.</p>
                    </div>
                </template>
                <template v-if="keywords.includes('Lifesteal')">
                    <h5>Lifesteal</h5>
                    <div class="keyword-description">
                        <p>A unit with lifesteal regenerates health when dealing damage to a unit.</p>
                        <p>In the case of combat damage, the healing happens at the same time as damage is dealt, similiar to regeneration</p>
                    </div>
                </template>
                <template v-if="keywords.includes('Heroic')">
                    <h5>Heroic</h5>
                    <div class="keyword-description">
                        <p>Heroic units are heroes and ascended creeps.</p>
                    </div>
                </template>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: ['color', 'name', 'manacost', 'type', 'height', 'attack', 'armor', 'health', 'crosslane', 'bg-image', 'bg-top-offset', 'tags', 'keywords', 'cost'],
    methods: {
        bgImageStyle(url, bgTopOffset) {
            return {'background-image': `url(${url})`,
                    'background-position': `50% ${bgTopOffset}`};
        },
        capitalize(str) {
            return str[0].toUpperCase() + str.substring(1);
        }
    },
    computed: {
        cardBg () {
            if (this.type === 'creep' || this.type === 'hero') {
                return require(`../assets/card_bg_${this.color}.png`);
            }
            else if (this.type !== 'hero') {
                return require(`../assets/card_bg_spell_${this.color}.png`);
            } else {
                return require(`../assets/card_bg_${this.color}.png`);
            }
        },
        cardTypeIcon () {
            return require(`../assets/cardtype_${this.type}.png`);
        },
        width () {
            return this.height * 0.59;
        },
        classes () {
            let style = {card: true};
            style[this.type] = true;
            if (this.type === 'improvement' && (this.crosslane !== false) || this.crosslane) {
                style.crosslane = true;
            }
            return style;
        }
    }
}
</script>

<style lang="scss" scoped>

.card .detailed-information {
    display: block;
    position: fixed;
    left: 0;
    margin: auto;
    top: 1em;
    bottom: 1em;
    width: 500px;
    background: #333;
    box-shadow: 0 0 10px rgba(0,0,0,0.6) inset;
    transform: translateX(-700px);
    transition: transform 500ms;
    transition-delay: 250ms;
    padding: 2rem;

    h3 {
        border-bottom: 4px double #666;
    }

    p {
        margin-bottom: 0.5em;
    }

    .tags-value {
        font-style: italic;
    }

    .detailed-information-desc-text, .keyword-description {
        padding: 1rem 1rem;
        background: #222;
        color: #ddd;
        em {
            color: #fff;
        }
        p {
            font-size: 1.2rem;
            margin-top: 0.5rem;
            margin-bottom: 0.5rem;
        }
    }

    .keywords-clarification {
        h5 {
            margin-bottom: 0.5rem;
        }
    }

    .properties {
        display: grid;
        grid-row-gap: 0.5em;
        grid-template-columns: max-content max-content;
        font-size: 1.2rem;
        margin-bottom: 2rem;
        .property, .value {
            border-bottom: 1px solid #555;
        }
        .value {
            padding-right: 0.5em;
        }
        .property {
            &::after {
                content: ':';
                margin-right: 2em;
            }
        }
    }
}

.card {
    &:hover .detailed-information {
        transform: translateX(0);
        transition-delay: 0ms;
    }
    display: grid;
    grid-template-rows: 60px [card-art] 50fr [card-text] min-content [bottom] 80px;
    grid-template-columns: 1fr;
    color: #fff;
    z-index: 99;
    margin-right: 1em;
    &.spell, &.improvement, &.health, &.weapon, &.armor {
        grid-template-rows: 60px [card-art] 50fr [card-text] min-content [bottom] 16px;
    }
    &.crosslane .manacost {
        &::before, &::after {
            background: url('../assets/crosslane.png');
            content: ' ';
            position: relative;
            width: 16px;
            height: 16px;
            top: -3px;
            background-size: contain;
            display: inline-block;
        }
        &::after {
            transform: scaleX(-1);
        }
    }
    img {
        grid-row: 1 / -1;
        grid-column: 1 / 2;
        z-index: 2;
    }

    .cardtype-icon {
        grid-column: 1 / 2;
        grid-row-start: card-art;
        z-index: 99;
        position: relative;
        transform: scale(0.65);
        transform-origin: center;
        display: inline-block;
        margin-right: auto;
        margin-bottom: auto;
        position: relative;
        top: -4px;
    }
    .bg-image {
        grid-column: 1 / 2;
        grid-row-start: card-art;
        grid-row-end: bottom;
        background-size: cover;
        background-position: 50% 50%;
    }
    .bg-image:not([data-bg]) {
        background: grey;
        box-shadow: 0 0 50px rgba(0,0,0,0.5) inset;
        display: flex;
        align-items: center;
        justify-content: center;
        &::before {
            content: '?';
            font-size: 12rem;
            text-align: center;
            margin-bottom: auto;
            display: block;
            text-shadow: 5px 5px 3px rgba(0,0,0,0.5);
            position: relative;
            top: 3rem;
        }
    }

    .top {
        z-index: 3;
        grid-column: 1 / 2;
        grid-row: 1 / 2;
        display: flex;
        align-items: center;
        padding-left: 1rem;
        padding-top: 8px;
        .manacost {
            font-size: 2.25rem;
            margin-right: 0.75rem;
        }
        .name {
            font-size: 1.75rem;
            font-family: "RadianceC";
        }
        .itemcost {
            margin-left: auto;
            margin-right: 1rem;
            font-size: 2rem;
        }
    }

    .bg-desc {
        grid-column: 1 / 2;
        grid-row-start: card-text;
        background: url('../assets/card_desc_bg.png');
        background-repeat: no-repeat;
        z-index: 1;
        opacity: 0.6;
    }

    .desc-text {
        grid-column: 1 / 2;
        grid-row-start: card-text;
        min-height: 160px;
        padding: 1em;
        padding-bottom: 1em;
        z-index: 2;
        font-size: 1.25rem;
        display: flex;
        text-align: center;
        justify-content: center;
        grid-template-rows: 2fr [text] min-content 5fr;
        grid-template-columns: 1fr;
        display: grid;
        em {
            font-style: normal;
            color: #fff;
        }
        small {
            font-size: 0.85rem;
        }

        .tags {
            grid-row-start: 3;
            font-style: italic;
            text-align: right;
            margin-top: auto;
            font-size: 1rem;
            color: rgba(255,255,255, 0.75);
            position: relative;
            top: 1rem;
        }
        p {
            font-weight: 400;
            color: #ccc;
            line-height: 1.2;
            margin: 0;
        }
        & > p, & > div {
            margin: 0;
            grid-row-start: text;
            margin-top: 0.5rem;
            margin-bottom: 1rem;
        }
        p + p {
            margin-top: 1em;
        }
    }
    &.spell .desc-text, &.improvement .desc-text {
        min-height: 200px;
    }
    .bottom {
        grid-column: 1 / 2;
        grid-row-start: bottom;
        z-index: 4;
        display: flex;
        justify-content: space-around;
        align-items: center;
        font-size: 2rem;
        .attack:before, .armor:before, .health:before {
            content: ' ';
            background: url('../assets/attack.png');
            width: 1em;
            display: inline-block;
            height: 1em;
            background-size: cover;
            position: relative;
            top: 0.13em;
            margin-right: 0.1em;
        }
        .armor:before {
            background: url('../assets/armor.png');
            background-size: cover;
        }
        .health:before {
            background: url('../assets/health.png');
            background-size: cover;
        }
    }
}
</style>