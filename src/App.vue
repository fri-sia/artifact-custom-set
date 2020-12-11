<template>
  <div id="app">
    <img class="logo" src="https://steamcdn-a.akamaihd.net/apps/artifact/images/header/artifact_logo_header.png" alt="">
    <div class="side-art"><img src="./assets/races.jpg" alt=""></div>
    <div class="headline">
      <span>Introducing:</span>
      <h1>Artifact 2.0</h1>
      <p>
        <em>Get your pogchamps ready.</em>
        After the longest of hauls, the best card game of all time is back. We listened to your feedback and have an update ready to drop on the first of september. It will bring a brand new set, modding support and a complete rehaul of matchmaking and economy. And just as a little bonus we included Dr. Garfields death certificate in the patchnotes.
      </p>
    </div>

    <div class="full-row set-announce">
      <div class="bg-image"></div>
      <div class="text">
        <h2>Ascension, the first Artifact expansion</h2>
        <p>The battle rages on between The Red Mist and Bronze Legion. However the Vhouls aren't the only ones rising up against the tyranny this time, some parts of their armies has begun to lose trust in the commanders and offer an alternative way forward.</p>
        <h3>Are we heroes yet?</h3>
        <p>In this set we'll introduce a brand new mechanic: Ascend. Any unit that ascends into a color can play cards as if they were a hero of that color.</p>
        <div class="card-list">
          <card
            color="green"
            height="600"
            name="Vhoul Trickster"
            manacost="2"
            type="creep"
            attack="1"
            armor="0"
            health="4"
            bg-image="https://i.pinimg.com/564x/4e/de/d6/4eded622e9f8e709df5da81827dc19b1.jpg"
            tags="Vhoul wizard"
            :keywords="['Ascend']"
          >
            <template v-slot:description>
              <p><em>Ascend</em> as <span class="blue">blue</span>, for blue cards costing 3 or less.</p>
            </template>
          </card>
          <card
            color="black"
            height="600"
            name="Cultist of the Flayed Twins"
            manacost="5"
            type="creep"
            attack="3"
            armor="0"
            health="8"
            bg-image="https://i.pinimg.com/564x/fd/6a/4a/fd6a4adedd4c7965535f097ff0c041b5.jpg"
            bg-top-offset="0rem"
            tags="Cultist"
            keywords="['Ascend']"
          >
            <template v-slot:description>
              <p><span class="active">Active <span class="cd-icon"></span> 1:</span> Condemn an allied hero in any lane. <em>Ascend</em> as all colors of that hero until end of round.</p>
            </template>
          </card>

          <card
            color="blue"
            height="600"
            name="The Great Awakening"
            manacost="8"
            type="improvement"
            bg-image="https://i.pinimg.com/564x/b8/fe/a7/b8fea7187d200f4ddda65cb9212702c0.jpg"
            keywords="['Ascend']"
            tags="Radiant tribal improvement"
            >
            <template v-slot:description>
              <p>Allied Melee Creeps have<br/> “<em>Ascend</em> as <span class="blue">blue</span>”</p>
            </template>
          </card>
          <card
            color="red"
            height="600"
            name="Stonehall Champion"
            manacost="7"
            type="creep"
            attack="7"
            armor="2"
            health="7"
            bg-top-offset="0"
            bg-image="https://i.pinimg.com/564x/1c/87/b1/1c87b1cdd4daa70360f040fd13b5f542.jpg"
            keywords="['Ascend']"
            tags="Stonehall"
            >
            <template v-slot:description>
              <p><em>Ascend</em> as <span class="red">red</span>.</p>
            </template>
          ></card>
          <card
            color="blue"
            height="600"
            type="creep"
            attack="0"
            armor="0"
            health="7"
            manacost="7"
            name="Slumbering ogre"
            bg-image="https://i.pinimg.com/564x/fb/76/44/fb76449258fd82633a090b9df340c2c1.jpg"
            keywords="['Ascend']"
            tags="Ogre"
          >
            <template v-slot:description>
              <p><span class="active">Active <span class="cd-icon"></span> 1:</span> Until end of round, <em>ascend</em> as <span class="blue">blue</span>.</p>
            </template>
          </card>
          <card
            name="Brisso the Druid"
            color="green"
            bg-image="https://i.pinimg.com/564x/8e/2a/86/8e2a8627c1c575aca2270245f4f6d40b.jpg"
            type="creep"
            height="600"
            attack="2"
            armor="0"
            health="8"
            manacost="5"
            :keywords="['Ascend']"
            tags="Druid"
          >
            <template v-slot:description>
              <div>
                <p><span class="active">Active <span class="cd-icon"></span> 1:</span> spend 1 mana, <em>ascend</em> as <span class="green">green</span> for creeps until end of round.</p>
                <p>Whenever you play a creep,<br/> draw a card.</p>
              </div>
            </template>
          </card>
          <card
            name="Impersonator"
            type="creep"
            height="600"
            attack="6"
            health="5"
            armor="0"
            tags="Assasin"
            color="black"
            manacost="5"
            bg-image="https://i.pinimg.com/564x/3f/50/a9/3f50a9c75227d613c2239bc2e85d4720.jpg"
            :keywords="['Ascend']"
          >
            <template v-slot:description>
              <p>When an enemy neighbor hero dies, Impersonator <em>Ascends</em> as all colors of that hero.</p>
            </template>
          </card>
          <card
            name="Stonehall Siege Commander"
            type="creep"
            height="600"
            attack="2"
            armor="1"
            health="5"
            manacost="5"
            tags="Stonehall"
            color="red"
            bg-image="https://i.pinimg.com/564x/88/4b/47/884b4737faafcdcaa579e9af1139a50b.jpg"
            :keywords="['Ascend']"
          >
            <template v-slot:description>
              <p>Stonehall Siege Commander <em>Ascends</em> as <span class="black">black</span> for Constructs.</p>
            </template>
          </card>
        </div>
        <p>With all of these creeps ascending into heroic status, naturally this set will also feature cards requiring multiple colors. Transcend is another new mechanic, check it out on these cards:</p>
        <div class="card-list">
          <card
            color="green"
            height="600"
            name="Ashes to Ashes"
            bg-image="https://i.pinimg.com/564x/92/64/9a/92649ad3fd7cdf49c708eac3057f336d.jpg"
            manacost="1"
            type="spell"
            keywords="['Transcend']"
          >
            <template v-slot:description>
              <div>
                <p>
                  Condemn a unit. Heal your tower equal to the health of the unit.
                </p>
                <p>
                  <em>Transcend <span class="black">black</span></em>: Gain gold equal to the attack of the unit.
                </p>
              </div>
            </template>
          </card>
          <card
            color="red"
            height="600"
            name="Inner Beast"
            manacost="2"
            type="spell"
            bg-image="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/3c0dc955-b6ef-462a-b122-da644702a329/d88i7q0-d3385254-0c2d-4cde-ad14-193a61e574fc.jpg/v1/fill/w_1024,h_1366,q_75,strp/beast_of_the_wind_by_alexkonstad_d88i7q0-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9MTM2NiIsInBhdGgiOiJcL2ZcLzNjMGRjOTU1LWI2ZWYtNDYyYS1iMTIyLWRhNjQ0NzAyYTMyOVwvZDg4aTdxMC1kMzM4NTI1NC0wYzJkLTRjZGUtYWQxNC0xOTNhNjFlNTc0ZmMuanBnIiwid2lkdGgiOiI8PTEwMjQifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6aW1hZ2Uub3BlcmF0aW9ucyJdfQ.Wc76TiKlxzh5WIjDd0nQoiL9vzvPuTNx7YvtDpkJ3a0"
            keywords="['Transcend']"
          >
            <template v-slot:description>
              <div>
                <p>
                  Modify allied hero with +4 attack and -4 health.
                </p>
                <p>
                  <em>Transcend <span class="green">green</span></em>: replace “allied hero” with “unit”.
                </p>
              </div>
            </template>

          </card>
        </div>
        <p>A card with <em>Transcend &lt;color&gt;</em> will have an additional effect if you are able to play cards of the given color. Here are a few more.</p>
        <h3>Unsorted</h3>
        <div class="card-list">
          <card
            color="black"
            height="600"
            name="Infection"
            manacost="2"
            type="spell"
            bg-image="https://i.pinimg.com/564x/25/ab/fb/25abfb36a787f21de5f45e8d84c51e39.jpg"
            :keywords="[]"
          >
            <template v-slot:description>
              <div>
                <p>Modify a unit with “At the start of the action phase, deal 1 damage to this unit.” AND<p/>
                <p>“<em>Death effect:</em> add 2 copies of “Infection” to your opponents hand.”</p>
              </div>

            </template>
          </card>
          <card
            color="black"
            height="600"
            name="Something in the Water"
            manacost="4"
            type="improvement"
            bg-image="https://i.pinimg.com/564x/8e/df/30/8edf3015c8e8a4ea3d1ba4b2c66dc36f.jpg"
            :keywords="[]"
          >
            <template v-slot:description>
              <div>
                <p>Whenever a unit enters this lane, modify it with -1 attack and -2 health.</p>
              </div>
            </template>
          </card>
          <card
            name="Forced March"
            height="600"
            color="red"
            manacost="5"
            type="spell"
            bg-image="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/09be60de-acc5-437b-9ec6-a6589fab6547/d2gehmu-47baf0d9-bae1-4727-9f98-10ec41680704.jpg/v1/fill/w_1024,h_597,q_75,strp/imperials_marching_by_epson361_d2gehmu-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9NTk3IiwicGF0aCI6IlwvZlwvMDliZTYwZGUtYWNjNS00MzdiLTllYzYtYTY1ODlmYWI2NTQ3XC9kMmdlaG11LTQ3YmFmMGQ5LWJhZTEtNDcyNy05Zjk4LTEwZWM0MTY4MDcwNC5qcGciLCJ3aWR0aCI6Ijw9MTAyNCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl19.w8uIqEefqhG7Am6pcU4Z4RDKjDs47mzAGfETyAb0AyQ"
            :keywords="[]"
          >
            <template v-slot:description>
              <div>
                <p>Condemn half of allied creeps <i>(rounded down, chosen at random)</i></p>
                <p><span class="pulse"></span> Return all allied units to the fountain.</p>
              </div>
            </template>
          </card>
          <card
            color="red"
            height="600"
            name="Mobilization"
            manacost="5"
            type="spell"
            bg-image="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/5a25b97c-558f-4972-9102-7c162ad33647/d8d7uhx-4e065f6f-dd83-4de5-8480-376f4850e3b0.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzVhMjViOTdjLTU1OGYtNDk3Mi05MTAyLTdjMTYyYWQzMzY0N1wvZDhkN3VoeC00ZTA2NWY2Zi1kZDgzLTRkZTUtODQ4MC0zNzZmNDg1MGUzYjAuanBnIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.17V25ylhzeF_7SkXo_0alN5DYNkAPJq9Pdxhheyd26s"
            :keywords="[]"
          >
            <template v-slot:description>
              <p>Your heroes in the fountain redeploy next round.</p>
            </template>
          </card>
          <card
            color="green"
            height="600"
            name="Shelter from the Wrath"
            manacost="6"
            :crosslane="false"
            type="improvement"
            bg-image="https://i.pinimg.com/564x/43/7a/9c/437a9c3cd234d8ebdadca42eec377539.jpg"
            :keywords="[]"
          >
            <template v-slot:description>
              <div>
                <p>At the start of the action phase, add a charge to this card. Then, if this has 2 charges on it, condemn this improvement and all units in all other lanes.</p>
              </div>
            </template>
          </card>
          <card
            color="blue"
            height="600"
            name="Cyclone"
            bg-image="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/598203c2-03ac-44ae-9d1c-46b57e0681f2/d834udx-22d09342-9442-490f-a813-d62408db3999.jpg/v1/fill/w_1024,h_1536,q_75,strp/typhoon_maker_by_gaudibuendia_d834udx-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9MTUzNiIsInBhdGgiOiJcL2ZcLzU5ODIwM2MyLTAzYWMtNDRhZS05ZDFjLTQ2YjU3ZTA2ODFmMlwvZDgzNHVkeC0yMmQwOTM0Mi05NDQyLTQ5MGYtYTgxMy1kNjI0MDhkYjM5OTkuanBnIiwid2lkdGgiOiI8PTEwMjQifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6aW1hZ2Uub3BlcmF0aW9ucyJdfQ.5XIFqHqPFf_p78_FDbhf7Gv3e61MKFG5zVMqXABrrqQ"
            manacost="4"
            type="spell"
            :keywords="['Banish']"
          >
            <template v-slot:description>
              <p>Banish a unit. The unit is redeployed into this lane next deployment phase. <i>(banished units have their health unchanged.)</i></p>
            </template>
          </card>
          <card
            color="green"
            height="600"
            name="Plot Armor"
            manacost="5"
            type="improvement"
            bg-image="https://orig00.deviantart.net/11e2/f/2014/024/b/7/armor_small_by_chaosringen-d73llq1.jpg"
            :keywords="[]"
          >
            <template v-slot:description>
              <p>Your tower has +1 armor for every allied hero.</p>
            </template>
          </card>
          <card
            color="blue"
            height="600"
            manacost="4"
            type="creep"
            attack="0"
            armor="0"
            health="6"
            name="Guardian of Selemene"
            bg-image="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/c2138ee1-5ca5-42cb-b83a-dbe50f2c8333/dbwu14g-fe9ff2d0-1415-41b2-a96b-144b600c1fbc.jpg/v1/fill/w_1600,h_1771,q_75,strp/aola___11__concept_art__by_fl00rmaster_dbwu14g-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9MTc3MSIsInBhdGgiOiJcL2ZcL2MyMTM4ZWUxLTVjYTUtNDJjYi1iODNhLWRiZTUwZjJjODMzM1wvZGJ3dTE0Zy1mZTlmZjJkMC0xNDE1LTQxYjItYTk2Yi0xNDRiNjAwYzFmYmMuanBnIiwid2lkdGgiOiI8PTE2MDAifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6aW1hZ2Uub3BlcmF0aW9ucyJdfQ.kQav623AwukuV6H6A9K9__-POGBDWsOJ1zrO5iw_Ggw"
            :keywords="[]"
          >
            <template v-slot:description>
              <p>Other allies have +3 armor while outside the combat phase.</p>
            </template>
          </card>
          <card
            height="600"
            type="spell"
            manacost="8"
            color="black"
            name="Throwing Bodies"
            bg-image="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/94c04d85-b6df-4dcc-bb1f-1c199003e539/daq3iu0-2b4d2825-f652-4f91-8e95-93c3978d714f.jpg/v1/fill/w_800,h_1201,q_75,strp/raise_me_now_by_rowye_daq3iu0-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9MTIwMSIsInBhdGgiOiJcL2ZcLzk0YzA0ZDg1LWI2ZGYtNGRjYy1iYjFmLTFjMTk5MDAzZTUzOVwvZGFxM2l1MC0yYjRkMjgyNS1mNjUyLTRmOTEtOGU5NS05M2MzOTc4ZDcxNGYuanBnIiwid2lkdGgiOiI8PTgwMCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl19.5P8EZF1Aod9POpp6klkG8OERGbf992MJXX--WkVaZbI"
            :keywords="[]"
          >
            <template v-slot:description>
              <p>Deal 5 damage to allied units. <span class="pulse"></span> deal 5 damage to the enemy tower for every allied unit.</p>
            </template>
          </card>
          <card
            name="Greed"
            type="spell"
            manacost="4"
            color="black"
            height="600"
            bg-image="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/e6e289bb-196d-4a15-bb3d-9fa433f61cff/d62k0nx-ead19c08-c799-428a-a348-478fbd91b72c.jpg/v1/fill/w_1024,h_1311,q_75,strp/greed_by_jasontn_d62k0nx-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9MTMxMSIsInBhdGgiOiJcL2ZcL2U2ZTI4OWJiLTE5NmQtNGExNS1iYjNkLTlmYTQzM2Y2MWNmZlwvZDYyazBueC1lYWQxOWMwOC1jNzk5LTQyOGEtYTM0OC00NzhmYmQ5MWI3MmMuanBnIiwid2lkdGgiOiI8PTEwMjQifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6aW1hZ2Uub3BlcmF0aW9ucyJdfQ.dRB9lOVzXE7qIob6NkR3MDiUTL9GDdTomDITMaZ7YJM"
            :keywords="[]"
          >
            <template v-slot:description>
              <p>Draw 4 cards, and modify each with +2 mana cost</p>
            </template>
          </card>
          <card
            name="The Code of Revtel"
            height="600"
            color="black"
            type="improvement"
            manacost="3"
            bg-image="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/7872cd1f-937d-4c6e-9473-4d5f7245ea76/d8qvidh-3cd4a031-a436-4d6f-80b5-15f396d1ed4c.jpg/v1/fill/w_900,h_1503,q_75,strp/black_blade_by_cglas_d8qvidh-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9MTUwMyIsInBhdGgiOiJcL2ZcLzc4NzJjZDFmLTkzN2QtNGM2ZS05NDczLTRkNWY3MjQ1ZWE3NlwvZDhxdmlkaC0zY2Q0YTAzMS1hNDM2LTRkNmYtODBiNS0xNWYzOTZkMWVkNGMuanBnIiwid2lkdGgiOiI8PTkwMCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl19.3Ys8Uz6JVgdH1g45qNrhnzvKoYkgzip94O5h6sWEUb8"
            :keywords="[]"
          >
            <template v-slot:description>
              <p>Silenced units have +3 bounty.</p>
            </template>
          </card>
          <card
            name="Big Game Hunter"
            height="600"
            color="black"
            type="creep"
            attack="3"
            armor="2"
            health="4"
            manacost="6"
            bg-image="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/1333332e-89a8-41f7-922d-812204b18721/dda22aj-ba9d9ace-bded-457c-8dc7-d867f3c7ce18.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzEzMzMzMzJlLTg5YTgtNDFmNy05MjJkLTgxMjIwNGIxODcyMVwvZGRhMjJhai1iYTlkOWFjZS1iZGVkLTQ1N2MtOGRjNy1kODY3ZjNjN2NlMTgucG5nIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.WK8CmxMIDNppvLvWidHFVOJxLTLSbMf3Xbdz4LRNxPM"
            bg-top-offset="0"
            :keywords="[]"
            tags="Hunter"
          >
            <template v-slot:description>
              <p>When blocked by a unit, Big Game Hunter gains attack equal to the bounty of the blocking unit.</p>
            </template>
          </card>
          <card
            name="Recruit"
            type="spell"
            color="red"
            manacost="7"
            height="600"
            bg-image="https://i.pinimg.com/564x/96/5c/e6/965ce63298b6b94cc8d91ab7ad4f4524.jpg"
            :keywords="['Tribal']"
            tags="Stonehall tribal spell"
          >
            <template v-slot:description>
              <p>Choose a stonehall creep in your deck. Add 3 copies of it to your hand.</p>
            </template>
          </card>
          <card
            name="Aiushtha’s Disciple"
            type="creep"
            color="green"
            height="600"
            manacost="7"
            attack="4"
            armor="4"
            health="4"
            bg-top-offset="0"
            bg-image="https://i.pinimg.com/564x/cc/f3/44/ccf3442a87f8b232d9db46934fca99f3.jpg"
            :keywords="[]"
            tags="Dryad"
          >
            <template v-slot:description>
              <div>
                <p>+4 Regeneration</p>
                <p>If any allied unit would be condemned by a card effect, set its health to it's regeneration instead.</p>
              </div>
            </template>
          </card>
          <card
            name="Chain of Command"
            type="spell"
            color="red"
            manacost="3"
            height="600"
            bg-image="https://i.pinimg.com/564x/1a/8d/7a/1a8d7adce1f1890f57f21cc5e8922629.jpg"
            :keywords="[]"
          >
            <template v-slot:description>
              <p>Silence all creeps. Draw a card.</p>
            </template>
          </card>
          <card
            name="Expedition to Icewrack"
            bg-image="https://i.pinimg.com/564x/6d/79/6b/6d796be586581715aee9725ea9773d62.jpg"
            height="600"
            color="black"
            type="improvement"
            manacost="4"
            :keywords="[]"
            tags="Expedition"
          >
            <template v-slot:description>
              <div style="font-size: 1rem;">
                <p><span class="active">Active <span class="cd-icon"></span> 1: </span>Spend 3 gold, and add 3 quest counters.</p>
                <p><span class="active">Active <span class="cd-icon"></span> 1: </span>Condemn Expedition to Icewrack and search your deck or hand for a creep with manacost equal to or less than the amount of quest counters and play it, ignoring color restrictions.</p>
              </div>
            </template>
          </card>
          <card
            name="Starved Vhoul"
            color="black"
            type="creep"
            height="600"
            manacost="2"
            attack="2"
            health="1"
            armor="0"
            bg-image="https://i.pinimg.com/564x/bf/c2/71/bfc271d18210f6f1f6778eb9aed24ee9.jpg"
            :keywords="['Lifesteal']"
            tags="Vhoul"
          >
            <template v-slot:description>
              <p><em>Lifesteal</em></p>
            </template>
          </card>
          <card
            name="Deceitful Wolf"
            color="green"
            type="creep"
            height="600"
            attack="3"
            health="3"
            armor="0"
            manacost="4"
            tags="Lycantrophe"
            :keywords="['Transcend']"
            bg-image="https://i.pinimg.com/564x/45/a4/92/45a4920214d90a214d84b4483d7f809b.jpg"
          >
            <template v-slot:description>
              <div style="font-size: 0.9em;">
                <p>After the combat phase, modify <em>Deceitful Wolf</em> with +2 health.</p>
                <p>Transcend <span class="black">black</span>: Also modify it with +2 siege after the combat phase.</p>
              </div>
            </template>
          </card>
          <card
            color="blue"
            height="600"
            type="creep"
            attack="0"
            armor="1"
            health="8"
            manacost="6"
            name="Meditation Statue"
            bg-image="https://i.pinimg.com/564x/7f/17/f7/7f17f74a5e66763480d2767ea80d93a2.jpg"
            :keywords="['Ascend']"
            tags="Statue"
          >
            <template v-slot:description>
              <p>Meditation Statue has “<em>Ascend</em> as all colors” while all allied heroes are in the fountain.</p>
            </template>
          </card>
          <card
            color="green"
            height="600"
            type="creep"
            attack="0"
            armor="1"
            health="8"
            manacost="6"
            bg-image="https://i.pinimg.com/564x/74/7f/1d/747f1da09ebc034600cbd04c6eeb8cb7.jpg"
            name="Vigilance Statue"
            :keywords="[]"
            tags="Statue"
          >
            <template v-slot:description>
              <p>Other allies have <em>Damage Immunity</em> while there are no allied heroes in lane.</p>
            </template>
          </card>
          <card
            color="black"
            height="600"
            type="creep"
            attack="0"
            armor="1"
            health="8"
            manacost="6"
            bg-image="https://i.pinimg.com/564x/31/5e/32/315e32376914a3211a5e22db4f21fb11.jpg"
            name="Fallen Statue"
            :keywords="[]"
            tags="Statue"
          >
            <template v-slot:description>
              <p>Allies have +3 <em>siege</em> while there are no allied heroes in lane.</p>
            </template>
          </card>
          <card
            color="red"
            height="600"
            type="creep"
            attack="0"
            armor="1"
            health="8"
            manacost="6"
            bg-image="https://i.pinimg.com/564x/69/74/3f/69743f3e63f0947de1f6de15a96e9455.jpg"
            :keywords="[]"
            tags="Statue"
            name="War Statue"
          >
            <template v-slot:description>
              <p>Allied heroes have +4 <em>cleave</em>, +4 attack and +4 armor while there are no allied heroes in your other lanes.</p>
            </template>
          </card>
          <card
            color="black"
            height="600"
            type="improvement"
            manacost="1"
            name="Order by the Coin"
            :keywords="[]"
            bg-image="https://i.pinimg.com/564x/76/c5/ad/76c5ad5d9b453289322e607ecce7b2a4.jpg"
          >
            <template v-slot:description>
              <p>
                After the combat phase, modify enemy units that dealt combat damage to your tower with +1 bounty.
              </p>
            </template>
          </card>
          <card
            color="black"
            height="600"
            type="creep"
            manacost="4"
            attack="4"
            armor="0"
            health="2"
            :keywords="['Transcend']"
            tags="Assasin"
            name="Ambitious Assasin"
            bg-image="https://i.pinimg.com/564x/ab/30/40/ab304086f68aeb22e0b011f8f207fed2.jpg"
          >
            <template v-slot:description>
              <div>
                <p><span class="active">Active <span class="cd-icon"></span> 1:</span> Deal X damage to a creep, where X is the bounty of the creep.</p>
                <p><em>Transcend <span class="red">red</span></em>: replace “creep” with “hero”.</p>
              </div>
            </template>
          </card>
          <card
            color="green"
            height="600"
            type="creep"
            manacost="2"
            attack="0"
            armor="0"
            health="2"
            name="Vhoul Baby"
            :keywords="[]"
            tags="Vhoul"
            bg-image="https://i.pinimg.com/564x/70/3e/fb/703efbe414204ff28148851874f2c567.jpg"
          >
            <template v-slot:description>
              <p><span class="active">Death effect:</span> Modify the units that dealt lethal damage to this card with +5 bounty.</p>
            </template>
          </card>
          <card
            color="green"
            height="600"
            type="creep"
            manacost="5"
            attack="3"
            armor="0"
            health="9"
            name="Siege Rhino"
            tags="Rhino"
            bg-image="https://i.pinimg.com/564x/79/9d/25/799d2514103ebb35f2e3a3cfa7ac0d17.jpg"
            :keywords="[]"
            bg-top-offset="-60px"
          >
            <template v-slot:description>
              <p>Siege Rhino has +X <em>siege</em>, where X is your tower’s remaining mana.</p>
            </template>
          </card>
          <card
            color="item"
            height="600"
            type="health"
            :keywords="[]"
            name="Soul Ring"
            cost="7"
            bg-image="https://i.pinimg.com/564x/66/21/7e/66217eb31ce764dd697e1018a78a9708.jpg"
          >
            <template v-slot:description>
              <div>
                <p>Equipped hero has +4 health.</p>
                <p><span class="active">Active <span class="cd-icon"></span> 1:</span> deal 4 piercing damage to equipped hero. Give your tower +1 mana until end of round, and restore 3 mana to your tower.</p>
              </div>
            </template>
          </card>
          <card
            color="item"
            height="600"
            type="weapon"
            name="Staff of the Teacher"
            cost="5"
            bg-image="https://i.pinimg.com/564x/13/c5/84/13c584c8cc53935d13909ec57addab93.jpg"
            :keywords="[]"
          >
            <template v-slot:description>
              <div>
                <p>Equipped hero has +2 attack</p>
                <p><span class="active">Active <span class="cd-icon" /> 2: </span>Add a <em>Combat Training</em> to your hand.</p>
              </div>
            </template>
          </card>
          <card
            color="blue"
            height="600"
            type="spell"
            name="Fatigue"
            manacost="5"
            :keywords="['Transcend']"
            bg-image="https://i.pinimg.com/564x/4d/73/8d/4d738dbd2159f810a7697de49d212006.jpg"
          >
            <template v-slot:description>
              <div>
                <p>Modify the enemy tower with -2 mana. Your enemy draws 2 cards.</p>
                <p><em>Transcend <span class="black">black</span></em>: Your enemy plays a copy of this card.</p>
              </div>
            </template>
          </card>
          <card
            color="green"
            height="600"
            type="improvement"
            manacost="6"
            name="Devotion"
            bg-image="https://i.pinimg.com/564x/b0/3c/02/b03c02c7b64dfb338bf5832c68729ee6.jpg"
            :keywords="['Heroic']"
          >
            <template v-slot:description>
              <p>Cards in your hand costs 1 less for each allied <em>Heroic</em> of the same color.</p>
            </template>
          </card>
          <card
            color="blue"
            height="600"
            type="spell"
            manacost="8"
            name="Chain Lightning"
            bg-image="https://i.pinimg.com/564x/31/47/c1/3147c1359637848ac9696e588d9a68fb.jpg"
            :keywords="['Heroic']"
            tags="Lightning"
          >
            <template v-slot:description>
              <p>Deal 4 damage to the enemy tower for every <span class="blue">blue </span> <em>Heroic</em>.</p>
            </template>
          </card>
          <card
            color="red"
            height="600"
            type="spell"
            manacost="3"
            name="Only Heroes"
            bg-image="https://i.pinimg.com/564x/27/de/84/27de846ddfe2cdd76b2e3862f50c92e7.jpg"
            :keywords="['Heroic']"
          >
            <template v-slot:description>
              <p>Condemn a <em>Heroic</em> creep.</p>
            </template>
          </card>
          <card
            name="Deviant Studies"
            height="600"
            color="blue"
            bg-image="https://i.pinimg.com/564x/3d/89/b0/3d89b0f3fe7824749418be399d5052f2.jpg"
            manacost="3"
            type="improvement"
            :keywords="['Transcend']"
          >
            <template v-slot:description>
              <p>Your non-<span class="blue">blue</span> spells have “<em>Transcend </em> <span class="blue">blue</span>: Draw a card.”</p>
            </template>
          </card>
          <card
            name="Mountain Ridge"
            color="green"
            bg-image="https://i.pinimg.com/564x/44/65/cc/4465cc8fdab2f31a2e490aaae15f9b24.jpg"
            height="600"
            manacost="6"
            type="creep"
            attack="0"
            armor="6"
            health="6"
            :keywords="[]"
            tags="Landscape feature"
          >
            <template v-slot:description>
              <div>
                <p>Disarmed, +4 retaliate.</p>
                <p>Enemy neighbors are unaffected by <em>siege</em>.</p>
              </div>
            </template>
          </card>
          <card
            name="Medallion of Courage"
            cost="9"
            color="item"
            height="600"
            bg-image="https://images2.sw-cdn.net/product/picture/710x528_28263069_12652573_1563260555.jpg"
            type="armor"
            :keywords="[]"
          >
            <template v-slot:description>
              <div>
                <p>Equipped hero has +2 armor.</p>
                <p><span class="active">Active <span class="cd-icon" /> 1:</span> Until end of round, equipped hero has -2 armor and target unit has +2 armor.</p>
              </div>
            </template>
          </card>
          <card
            name="War Elephant"
            manacost="8"
            color="green"
            type="creep"
            attack="8"
            health="16"
            armor="1"
            :keywords="['Transcend']"
            bg-image="https://i.pinimg.com/564x/92/61/a4/9261a429b4d791236627332bc5313ed2.jpg"
            height="600"
          >
            <template v-slot:description>
              <div>
                <p><em>Transcend <span class="red">red</span></em>: at the start of the action phase, <em>War Elephant</em> battles the unit blocking it.</p>
              </div>
            </template>
          </card>
          <card
            name="Beefcake Hydra"
            height="600"
            bg-image="https://i.pinimg.com/564x/fe/39/ef/fe39ef6aa39284fafc058555fb222997.jpg"
            manacost="6"
            type="creep"
            attack="1"
            health="5"
            color="green"
            armor="0"
            :keywords="[]"
          >
            <template v-slot:description>
              <p>After <em>Beefcake Hydra</em> takes damage, double it's attack and health.</p>
            </template>
          </card>
          <card
            name="Oglodi Ballista"
            height="600"
            bg-image="https://i.pinimg.com/564x/a5/0f/2b/a50f2bb97795f63bc0467d4a10b1ed06.jpg"
            color="black"
            type="creep"
            attack="0"
            armor="0"
            health="4"
            manacost="4"
            tags="Red Mist Construct"
            :keywords="[]"
          >
            <template v-slot:description>
              <p><span class="active">Active <span class="cd-icon" /> 3:</span> Deal 10 piercing damage to <em>Oglodi Ballista</em>’s combat target.</p>
            </template>
          </card>
          <card
            name="Infiltrate the Stashes"
            color="black"
            type="spell"
            manacost="5"
            :keywords="[]"
            tags=""
            height="600"
            bg-image="https://i.pinimg.com/564x/08/d8/a0/08d8a0f8f30a9c2784257178419184b3.jpg"
          >
            <template v-slot:description>
              <div style="font-size: 1.1rem;">
              <p>Reveal 3 cards from your enemy’s item deck. Choose one among them, and modify it <em>secretely</em> with: </p>
              <p>“<span class="active">Play effect:</span> Ignore any other text on this card. Condemn this item and summon a <em>Mimic</em> on your enemy’s side. Gain gold equal to the cost of this item.”</p>
              </div>
            </template>
          </card>
          <card
            name="Mimic"
            color="black"
            type="creep"
            :keywords="[]"
            attack="5"
            health="5"
            armor="0"
            height="600"
            tags="Mimic"
            bg-image="https://i.pinimg.com/564x/3a/ab/8c/3aab8cee7734793a13547cade01e9323.jpg"
          ></card>
          <card
            name="Forest Guardian"
            height="600"
            type="creep"
            color="green"
            manacost="4"
            attack="4"
            armor="0"
            health="4"
            bg-image="https://i.pinimg.com/564x/f7/be/a9/f7bea9c1e8a33f897359f589d70354da.jpg"
            :keywords="[]"
            tags="Treant"
          >
            <template v-slot:description>
              <p>After your enemy plays a non-item card, restore 3 mana to your tower.</p>
            </template>
          </card>
          <card
            height="600"
            name="Noface"
            type="creep"
            color="black"
            attack="6"
            armor="0"
            health="6"
            manacost="6"
            :keywords="[]"
            tags="Spirit"
            bg-image="https://i.pinimg.com/564x/01/46/77/0146771a620824dc38cd21bfeb834693.jpg"
          >
            <template v-slot:description>
              <div style="font-size: 1.1rem;">
                <p>At the start of the upkeep, add a charge on <em>Noface</em>. Then, each player condemns a unit for every charge.</p>
                <p>When a unit dies, modify <em>Noface</em> with +1 attack and +1 health.</p>  
              </div>
            </template>
          </card>
          <card
            height="600"
            name="Techies"
            type="hero"
            color="blue"
            armor="1"
            attack="2"
            health="6"
            bg-image="https://i.pinimg.com/564x/a8/fd/54/a8fd54e33f0b349f561ebce122e6f99b.jpg"
            :keywords="[]"
            tags=""
          >
            <template v-slot:description>
              <p>Deploy a proximinity mine to your opponents side each deployment phase.</p>
            </template>
          </card>
          <card
            height="600"
            name="Proximiity Mine"
            type="creep"
            color="blue"
            :keywords="[]"
            attack="0"
            armor="2"
            health="2"
            tags="Construct"
            bg-image="https://gamepedia.cursecdn.com/dota2_gamepedia/8/8b/Techies_Proximity_Mine_model.png?version=62f899e90279c03137d87a59ff4f8725"
          >
            <template v-slot:description>
              <p><span class="active">Death effect:</span> Deal 4 piercing damage to allied neighbors.</p>
            </template>
          </card>
          <card
            height="600"
            name="Keeper of the Light"
            bg-image="https://3.bp.blogspot.com/-JqrEC1Tncso/WKpcprF5MdI/AAAAAAAAhBk/gfaupZClcjMYz5AroiR9uUtP9JGkl0PSgCLcB/s1600-d/Keeper_of_the_Light_Ezalor_DOTA_2_Wallpaper_Fondo_Loading_screen.jpg"
            type="hero"
            color="blue"
            attack="2"
            armor="0"
            health="7"
            :keywords="[]"
            tags="Human Wizard"
          >
            <template v-slot:description>
              <p>At the end of the round, both towers in this lane get +1 max mana.</p>
            </template>
          </card>
          <card
            height="600"
            name="Illuminating Blast"
            bg-image="https://media.esportsedition.com/wp-content/uploads/2017/05/Keeper-1068x530.jpg"
            type="spell"
            color="blue"
            :keywords="[]"
            manacost="X"
          >
            <template v-slot:description>
              <p>Choose a blue hero and choose one:<br/>
              <small>Deal X damage to enemy units <em>left </em> of that hero.</small><br/>
              <small>Deal X damage to enemy units <em>right</em> of that hero.</small></p>
            </template>
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/a1/89/f6/a189f656269b5de642240eda6d291f5d.jpg"
            color="black"
            type="spell"
            height="600"
            name="Prepared Counterattack"
            :keywords="[]"
            manacost="5"
          >
            <template v-slot:description>
              <p>Modify units in your fountain with “When redeployed, deal 4 piercing damage to this units combat target”</p>
            </template>
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/39/93/f6/3993f6b413916891e94cfe9aae01f21e.jpg"
            color="green"
            type="creep"
            :keywords="[]"
            manacost="5"
            attack="4"
            armor="1"
            health="6"
            name="Lone Traveler"
            tags="Human Traveler"
            height="600"
          >
            <template v-slot:description>
              <p>After the combat phase, return <em>Lone Traveler</em> to the fountain.</p>
            </template>
          </card>
          <card
            color="item"
            type="weapon"
            bg-image="https://i.pinimg.com/564x/93/c8/33/93c833827fe942a72146e1b526771509.jpg"
            cost="16"
            height="600"
            :keywords="[]"
            name="Relic Sword"
          >
            <template v-slot:description>
              <div>
                <p>Equipped unit has +4 attack.</p>
                <p><span class="active">Equip effect:</span> Equipped unit battles with its combat target.</p>
                <p>After the round, if this card is in your hand, modify it with “Equipped unit has +2 attack”</p>
              </div>
            </template>
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/fd/6a/29/fd6a29cdb59721accf37a431147c301c.jpg"
            type="creep"
            color="blue"
            manacost="3"
            name="Battle Maiden"
            attack="3"
            armor="3"
            health="3"
            :keywords="[]"
            tags="Human Warrior"
            height="600"
          >
            <template v-slot:description>
              <p>You can't play spells in this lane.</p>  
            </template>  
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/bd/9b/e9/bd9be9e1ff39dbb7017c333caa7a8271.jpg"
            type="improvement"
            color="green"
            name="Expedition"
            manacost="5"
            :keywords="['Banish']"
            height="600"
          >
            <template v-slot:description>
              <div>
                <p><span class="active">Play effect:</span> banish the top 3 cards of your deck.</p>
                <p>While this is the active lane, cards banished by <em>Expedition</em> are in your hand.</p>
              </div>
            </template>
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/3f/ae/f4/3faef458dddad07c1b2aa25e1c760ff2.jpg"
            name="Guardian Spirit of the Forest"
            type="creep"
            color="green"
            height="600"
            manacost="2"
            attack="2"
            armor="0"
            health="2"
            :keywords="[]"
            tags="Spirit"
          >
            <template v-slot:description>
              <p>After the combat phase, shuffle this unit into your deck. Modify it with +2 manacost and double it's base attack and health.</p>
            </template>
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/39/64/95/396495c5b62ed0fd5432112d8aece62b.jpg"
            color="item"
            type="health"
            name="Aghanim’s Scepter"
            cost="16"
            :keywords="[]"
            height="600"
          >
            <template v-slot:description>
              <div>
                <p>Equipped hero has +6 health</p>
                <p><span class="active">Active <span class="cd-icon"></span> 2:</span> Add a base copy of equipped hero’s signature card.</p>
              </div>
            </template>
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/b7/f7/af/b7f7af484f9a1363995d23c752a67b23.jpg"
            name="Burrowing Worm"
            height="600"
            color="green"
            manacost="4"
            type="creep"
            attack="5"
            armor="0"
            health="5"
            :keywords="[]"
          >
            <template v-slot:description>
              <p>Whenever you pass, <em>Burrowing Worm</em> gains +1 armor until end of round.</p>
            </template>
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/f9/55/1a/f9551a7118be02affaa2823e590928c9.jpg"
            name="Tax Collector"
            height="600"
            color="black"
            manacost="3"
            type="creep"
            attack="1"
            health="5"
            armor="0"
            :keywords="[]"
            tags="Human"
          >
            <template v-slot:description>
              <p>Whenever you pass, gain 2 gold.</p>
            </template>
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/d9/37/02/d9370287a22b7c246415b242d8d7fdab.jpg"
            name="Impatient Fighter"
            height="600"
            color="red"
            manacost="7"
            type="creep"
            attack="7"
            armor="2"
            health="4"
            :keywords="[]"
            tags="Human Warrior"
          >
            <template v-slot:description>
              <p>Whenever you pass while this is in your hand, give this card -1 manacost until end of action phase.</p>
            </template>
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/f3/3e/bc/f33ebc1d2cf5d08344f8b84934af938a.jpg"
            name="Tower Colossus"
            height="600"
            color="black"
            type="creep"
            manacost="5"
            attack="4"
            health="4"
            armor="0"
            :keywords="[]"
            tags="Construct"
          >
            <template v-slot:description>
              <p>At the end of the combat phase, deal 4 damage to your tower and give <em>Tower Colossus</em> +4 attack and +4 health.</p>
            </template>
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/b8/e7/7e/b8e77ef84bc5cb647eb13255aff39950.jpg"
            name="Animate the Rubble"
            height="600"
            color="green"
            manacost="6"
            type="improvement"
            :keywords="[]"
          >
            <template v-slot:description>
              <p>During the deployment phase, if your tower took damage last turn, deploy a <em>Debris Golem</em> with X attack and X health into this lane.
              X is the damage that was dealt to your tower last turn.</p>
            </template>
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/ac/69/08/ac69081ea4744beb80cad2f49a711fcb.jpg"
            name="Kidnap"
            height="600"
            color="black"
            manacost="4"
            type="spell"
            :keywords="[]"
          >
            <template v-slot:description>
              <p>Choose an enemy creep with 4 or less attack in any lane. Take control of it and return it to the fountain.</p>
            </template>
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/7b/96/3e/7b963e66139affd6cd1c95840841193c.jpg"
            name="Flash Farm"
            height="600"
            color="black"
            manacost="5"
            type="spell"
            :keywords="[]"
          >
            <template v-slot:description>
              <p>Condemn all <em>Melee Creeps</em>.</p>
            </template>
          </card>
          <card
            bg-image="https://i.pinimg.com/564x/ff/ea/82/ffea8294bf5c226016bb38f188d5b759.jpg"
            name="Roseleaf Protector"
            height="600"
            color="green"
            manacost="4"
            type="creep"
            attack="4"
            armor="0"
            health="4"
            :keywords="[]"
          >
            <template v-slot:description>
              <p>When you could play this card, you may reveal it instead and draw a card. If this effect is activated, give <em>Roseleaf Protector</em> +2 lock.</p>
            </template>
          </card>
          <card
            color="item"
            height="600"
            type="armor"
            :keywords="[]"
            name="Nether Shrawl"
            cost="5"
            bg-image="https://i.pinimg.com/564x/b2/9b/48/b29b4854a27586fb94280bd875d6c022.jpg"
          >
            <template v-slot:description>
              <div>
                <p>Equipped hero has -3 armor.</p>
                <p>Equipped hero has <b>damage immunity</b> outside of the combat phase.</p>
              </div>
            </template>
          </card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Card from './components/Card.vue';

export default {
  name: 'app',
  components: {
    Card
  }
}
</script>

<style lang="scss">

.red {
  color: #8E2821;
}

.blue {
  color: #64A5BE;
}

.black {
  color: #837581;
}

.green {
  color: #3F782A;
}

.pulse {
  background: url('./assets/pulse.png');
  display: inline-block;
  width: 0.8em;
  height: 0.8em;
  background-size: cover;
  position: relative;
  top: 0.1em;

}

.active {

  color: #b3a183;
  .cd-icon {
    background: url('./assets/cd.png');
    display: inline-block;
    width: 0.8em;
    height: 0.8em;
    background-size: cover;
    position: relative;
    top: 0.1em;
    left: 0.1em;
  }
}

$background-color: #161616;

body {
  background: $background-color;
  text-shadow: 1px 1px 3px rgba(0,0,0,1);
  color: #707d7c;
  font-size: 24px;
  margin: 0;
}

p {
  line-height: 1.5;
  font-weight: 300;
}

h1, h2, h3, h4, h5, h6 {
  color: #ccc;
}

*, *:after, *:before {
  box-sizing: border-box;
}

$grid-cols: 2fr [main-content] minmax(600px, 900px) 1fr;

.full-row {
  grid-template-columns: $grid-cols;
  display: grid;
  grid-column: 1 / -1;
  grid-gap: inherit;
}

#app {
  font-family: 'Radiance', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: auto;
  margin-top: 1em;
  display: grid;
  grid-template-columns: $grid-cols;
  grid-gap: 4rem;
  .logo, .headline {
    grid-column-start: main-content;
  }
  .side-art {
    grid-column-start: 1;
    box-shadow: 1px -1px 2px rgba(255, 255, 255, 0.2);
    img {
      object-fit: cover;
      height: 100%;
      width: 100%;
    }
  }
}

h1 {
  font-size: 5rem;
  color: #ccc;
}

em {
  color: #ccc;
  font-style: normal;
}

.headline {
  line-height: 1;
  padding: 2rem 0;
  em {
    color: #ccc;
    font-style: normal;
    display: block;
    margin-bottom: 0.25em;
    font-weight: 400;
  }
  span {
    font-size: 3rem;
  }
}

@font-face {
  font-family: "Radiance";
  font-weight: 300;
  src: url('./assets/Radiance-Light.otf');
}

@font-face {
  font-family: "Radiance";
  font-weight: 400;
  src: url("https://artifaction-gg.firebaseapp.com/fonts/Radiance-Regular.9c101937a0c9c618642e37d042ad230d.otf") format("opentype");
  font-style: normal;
  font-weight: normal;
}

@font-face {
  font-family: "RadianceC";
  src: url("https://artifaction-gg.firebaseapp.com/fonts/Radiance-RegularCondensed.76a114de88b3f45ba427eb5c35163b90.otf") format("opentype");
  font-style: normal;
  font-weight: normal;
}

.set-announce {
  .bg-image {
    grid-column: 1 / 4;
    grid-row-start: 1;
  }
  .text {
    padding: 8rem 0;
    grid-column: 2 / 3;
    grid-row-start: 1;
  }
}

.card-list {
  display: flex;
  flex-flow: row;
  flex-wrap: wrap;
  .card {
    margin-bottom: 1em;
  }
  &.nowrap {
    flex-wrap: nowrap;
  }
}

</style>
