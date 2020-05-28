<template>
  <v-tabs vertical fill-height>
    <v-tab class="text-none text-left">
      <!-- <v-icon left>mdi-account</v-icon> -->
      Introduction
    </v-tab>
    <v-tab>
      <!-- <v-icon left>mdi-lock</v-icon> -->
      <p class="text-none text-left">Prevention</p>
    </v-tab>
    <v-tab class="text-none text-left">
      <!-- <v-icon left>mdi-access-point</v-icon> -->
      Treatment
    </v-tab>
    <v-tab class="text-none text-left">
      <!-- <v-icon left>mdi-account</v-icon> -->
      Myths and Facts
    </v-tab>
    <v-tab class="text-none text-left">
      <!-- <v-icon left>mdi-account</v-icon> -->
      Quiz
    </v-tab>

    <v-tab-item>
      <v-carousel fill-height>
        <v-carousel-item>
          <!-- <br /> -->
          <h1 class="display-2 font-weight-black text-center">
            Learn about COVID-19
          </h1>
          <hr />
          <v-row class="fill-height" align="center" justify="center">
            <img src="~assets/covidscare.jpg" width="900" />
          </v-row>
        </v-carousel-item>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            What is COVID-19?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            COVID-19, otherwise known as coronavirus disease 2019, is a new
            illness caused by a previously unknown virus called SARS-CoV-2. The
            virus is part of a family of coronaviruses which are responsible for
            lots of different illness from the common cold to the flu. But this
            new strain can be more severe in some populations. Discovered in
            December 2019, the virus has since spread around the world and on 11
            March, the World Health Organization (WHO) declared it pandemic.
          </p>
        </v-carousel-item>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            How is COVID-19 spread?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            COVID-19 is spread through contact with respiratory droplets of a
            person currently infected with the virus. These droplets come from
            the nose or mouth of an infected person and may land on surfaces and
            objects around them. The virus is then spread when another person
            comes into contact with these droplets and touches their own face,
            nose or mouth. The virus may also be spread when an infected person
            sneezes, coughs or exhales, and people around them breathe in these
            micro-droplets. For this reason, it’s important to stay around one
            meter (3 feet) away from someone you know to have the virus.
          </p>
        </v-carousel-item>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            What are the symptoms of COVID-19?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            The most common symptoms are a dry cough, tiredness and a high
            temperature. Other flu-like symptoms such as aches and pains, nasal
            congestion, runny nose, sore throat or diarrhoea are also common.
          </p>
          <p class="display-1 font-weight-medium">
            Around 80% of people with COVID-19 recover from the virus without
            the need for special treatment, usually in around seven days. Many
            may not even know that they have the virus, while others may feel
            like they have the common cold and treat it as they normally would
            at home. Around one in six people will get seriously ill from the
            virus and may have trouble breathing. These people will need
            hospitalisation.
          </p>
        </v-carousel-item>
        <v-carousel-item>
          <v-row class="fill-height" align="center" justify="center">
            <img src="~assets/signs.jpg" width="900" />
          </v-row>
        </v-carousel-item>
      </v-carousel>
    </v-tab-item>
    <v-tab-item>
      <v-carousel fill-height>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            How can I prevent COVID-19?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            The best way to stop coronavirus infection is through frequent
            washing of your hands and not touching your face. Use soap and water
            and wash for around 40 seconds, you can also use an alcohol-based
            hand sanitiser if you do not have access to water or soap. If you
            sneeze or cough, use a clean tissue to cover your mouth and nose,
            then make sure you throw it away after and wash your hands. If you
            don’t have a tissue, use the inside of your elbow to cover your
            mouth and nose.
          </p>
          <p class="display-1 font-weight-medium">
            Be sure to avoid close contact with anyone who has a fever or cough.
            Similarly, if you are feeling unwell, make sure you keep away from
            others.
          </p>
        </v-carousel-item>

        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            Should I wear a facemask?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            Using a facemask is only effective if you are working with someone
            known to have COVID-19 or if you are sneezing and coughing and are
            trying to protect others. They are only effective when used properly
            and disposed of safely. Wearing a mask should always be combined
            with frequent handwashing.
          </p>
        </v-carousel-item>
        <v-carousel-item>
          <v-row class="fill-height" align="center" justify="center">
            <img src="~assets/covidprotect.jpg" width="900" />
          </v-row>
        </v-carousel-item>
        <v-carousel-item>
          <!-- <v-row class="fill-height" align="center" justify="center">
            <img src="~assets/covidprotect.jpg" width="900" />
          </v-row> -->
          <v-container>
            <v-playback
              url="/handwashing.mp4"
              loop
              auto-play="play"
            ></v-playback>
          </v-container>
        </v-carousel-item>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            What is social or physical distancing?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            To prevent the spread of COVID-19, people are advised to keep their
            distance from others. The exact advice on how to do this will vary
            between countries. In some places, people have been asked to stop
            shaking hands and avoid large gatherings. Other places are advising
            people to stay at home completely and only leave the house to
            exercise, shop for essentials and go to work (if you can’t work at
            home).
          </p>
          <p class="display-1 font-weight-medium">
            The aim of this advice is to slow the spread of the virus by
            reducing the number of people you meet in a day. This will help the
            health system by preventing a large number of critical care patients
            presenting at the same time.
          </p>
        </v-carousel-item>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            Which populations are at-risk for severe COVID-19?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            The likelihood of serious illness increases in older populations and
            people with underlying health problems including high blood
            pressure, heart problems, lung disease or diabetes. There is
            currently no evidence to suggest that people living with HIV and on
            effective antiretroviral treatment are at an increased risk for
            acquiring COVID-19 or developing severe symptoms. See our page on
            COVID-19 and living with HIV.
          </p>
          <p class="display-1 font-weight-medium">
            Be sure to avoid close contact with anyone who has a fever or cough.
            Similarly, if you are feeling unwell, make sure you keep away from
            others.
          </p>
        </v-carousel-item>
      </v-carousel>
    </v-tab-item>
    <v-tab-item>
      <v-carousel fill-height>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            When do symptoms start to appear?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            It can take up to 14 days for people to show symptoms, but most
            people notice them in the first four to five days.
          </p>
          <!-- <p class="display-1 font-weight-medium">
            Be sure to avoid close contact with anyone who has a fever or cough.
            Similarly, if you are feeling unwell, make sure you keep away from
            others.
          </p> -->
        </v-carousel-item>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            What should I do if I think I have COVID-19?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            If you think you have COVID-19, stay at home and call your local
            health service for advice. Do not visit your clinic as you could
            pass the virus onto others. The people you live with should also
            stay home for at least 14 days from when you first noticed symptoms.
          </p>
          <p class="display-1 font-weight-medium">
            Avoid close contact with others in your household while you’re ill.
            If you live with someone who’s more vulnerable, try to arrange for
            them to stay elsewhere.
          </p>
        </v-carousel-item>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            Does COVID-19 need treatment?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            Around 80% of people who get COVID-19 will recover without needing
            special treatment at home, and usually within around seven days.
            Most people will only have mild symptoms similar to the common cold.
          </p>
          <p class="display-1 font-weight-medium">
            Around one in six people will become severely ill and develop
            difficulty breathing, in which case they will need hospital care. In
            serious cases COVID-19 can cause pneumonia.
          </p>
        </v-carousel-item>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            Can COVID-19 be cured?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            There’s no proven cure for COVID-19, but most people will recover
            fully without needing medical treatment. If you’re unwell with
            COVID-19, resting, drinking lots of liquids, and taking paracetamol
            or other home remedies can help with symptoms.
          </p>
          <p class="display-1 font-weight-medium">
            If your symptoms don’t improve after seven days or if you have
            difficulty breathing and persistent pain in your chest, call your
            local health service immediately.
          </p>
        </v-carousel-item>
      </v-carousel>
    </v-tab-item>
    <v-tab-item>
      <v-carousel fill-height>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            Will most people who get COVID-19 get very sick or die?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            FACT: Most people who get COVID­-19 will have a mild form of the
            illness and recover without needing professional medical care.
            Around eight out of every 10 people with COVID­-19 will have mild
            symptoms. Around one in six people will become severely ill and need
            hospital care. Scientific modelling suggests that around 1 in 100
            people who get COVID-19 will die.
          </p>
        </v-carousel-item>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            Can you always tell if someone has COVID-19?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            FACT: No The virus can be in someone’s body for up to 14 days before
            they get symptoms, and some people will have such a mild case of
            COVID-19 that they might not notice that anything is wrong. That’s
            why it’s important that everyone follows government advice –
            including hand washing, using tissues to catch coughs and sneezes,
            and avoiding crowds – to stop the spread of the virus, even if they
            feel healthy.
          </p>
        </v-carousel-item>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            Does COVID-19 only affect old people?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            FACT: While COVID-19 can be more dangerous in older people, anyone
            can get it including young people, some of whom become seriously
            ill. While we don’t yet fully understand why some people get more
            serious symptoms, we do know that young people are more likely to
            develop serious symptoms if they have certain underlying health
            conditions, for example asthma, heart conditions or untreated HIV.
          </p>
        </v-carousel-item>
        <v-carousel-item>
          <h1 class="display-2 font-weight-black text-center">
            Are people living with HIV more likely to get seriously ill?
          </h1>
          <hr />
          <br />
          <p class="display-1 font-weight-medium">
            FACT: If you are living with HIV and on effective treatment there's
            no evidence that you are at higher risk of developing serious
            COVID-19 symptoms. This is because your treatment will be keeping
            your immune system strong and your body able to deal with
            infections. If you are worried that you might have HIV, now is a
            good time to get tested so you can start treatment if you need it.
          </p>
        </v-carousel-item>
      </v-carousel>
    </v-tab-item>
    <v-tab-item>
      <v-carousel
        v-model="model"
        fill-height
        :show-arrows="false"
        hide-delimiters
      >
        <v-carousel-item>
          <v-container>
            <v-row>
              <p class="display-2 font-weight-black">
                Test your knowledge on COVID-19
              </p>
              <v-spacer></v-spacer>
              <v-btn
                outlined
                rounded
                large
                color="default"
                class="text-none"
                @click="model++"
                ><v-icon left>mdi-marker-check</v-icon>Start work</v-btn
              >
            </v-row>
          </v-container>

          <hr />
          <!-- <br /> -->

          <v-container text-center align-center justify-center>
            <img src="~assets/exams.svg" alt="exam svg" width="400vw" />
          </v-container>
        </v-carousel-item>
        <v-carousel-item>
          <v-container fluid>
            <h1 class="display-2 font-weight-black">
              How is COVID-19 passed on?
            </h1>
            <hr />
            <br />
            <v-radio-group class="display-1 font-weight-medium">
              <v-radio
                @click="response"
                label="Through droplets that come from your mouth and nose when you cough or breathe out"
                value="radio-1"
              ></v-radio>
              <v-radio
                @click="model++"
                label="In sexual fluids, including semen, vaginal fluids or anal mucous"
                value="radio-2"
              ></v-radio>
              <v-radio
                @click="model++"
                label="By drinking unclean water"
                value="radio-3"
              ></v-radio>
              <v-radio
                @click="model++"
                label="All of the above"
                value="radio-4"
              ></v-radio>
            </v-radio-group>
          </v-container>
        </v-carousel-item>
        <v-carousel-item>
          <v-container fluid>
            <h1 class="display-2 font-weight-black">
              What are the common symptoms of COVID-19?
            </h1>
            <hr />
            <br />
            <v-radio-group class="display-1 font-weight-medium">
              <v-radio
                @click="model++"
                label="A new and continuous cough "
                value="radio-1"
              ></v-radio>
              <v-radio @click="model++" label="Fever" value="radio-2"></v-radio>
              <v-radio
                @click="model++"
                label="Tiredness"
                value="radio-3"
              ></v-radio>
              <v-radio
                @click="response"
                label="All of the above"
                value="radio-4"
              ></v-radio>
            </v-radio-group>
          </v-container>
        </v-carousel-item>
        <v-carousel-item>
          <v-container fluid>
            <h1 class="display-2 font-weight-black">
              Can you always tell if someone has COVID-19?
            </h1>
            <hr />
            <br />
            <v-radio-group class="display-1 font-weight-medium">
              <v-radio
                @click="response"
                label="No – not everyone with COVID-19 has symptoms"
                value="radio-1"
              ></v-radio>
              <v-radio
                @click="model++"
                label="Yes – it will be obvious, a person with COVID-19 coughs a lot"
                value="radio-2"
              ></v-radio>
              <v-radio
                @click="model++"
                label="Yes – you can tell just by where a person comes from, their race and ethnicity"
                value="radio-3"
              ></v-radio>
            </v-radio-group>
          </v-container>
        </v-carousel-item>
        <v-carousel-item>
          <v-container fluid>
            <h1 class="display-2 font-weight-black">
              Can washing your hands protect you from COVID-19?
            </h1>
            <hr />
            <br />
            <v-radio-group class="display-1 font-weight-medium">
              <v-radio
                @click="model++"
                label="Yes – but only if you use a strong bleach"
                value="radio-1"
              ></v-radio>
              <v-radio
                @click="response"
                label="Yes – normal soap and water or hand sanitizer is enough"
                value="radio-2"
              ></v-radio>
              <v-radio
                @click="model++"
                label="No – Washing your hands doesn’t stop COVID-19"
                value="radio-3"
              ></v-radio>
            </v-radio-group>
          </v-container>
        </v-carousel-item>
        <v-carousel-item>
          <v-container fluid>
            <h1 class="display-2 font-weight-black">
              Which of the following people is COVID-19 more dangerous for?
            </h1>
            <hr />
            <br />
            <v-radio-group class="display-1 font-weight-medium">
              <v-radio
                @click="model++"
                label="Children "
                value="radio-1"
              ></v-radio>
              <v-radio
                @click="model++"
                label="African people"
                value="radio-2"
              ></v-radio>
              <v-radio
                @click="response"
                label="People with certain underlying health conditions "
                value="radio-3"
              ></v-radio>
              <v-radio
                @click="model++"
                label="European people"
                value="radio-4"
              ></v-radio>
            </v-radio-group>
          </v-container>
        </v-carousel-item>
        <v-carousel-item>
          <v-container fluid>
            <h1 class="display-2 font-weight-black">
              Are people living with HIV always more at risk?
            </h1>
            <hr />
            <br />
            <v-radio-group class="display-1 font-weight-medium">
              <v-radio
                @click="model++"
                label="Yes – people with HIV have weaker immune systems "
                value="radio-1"
              ></v-radio>
              <v-radio
                @click="response"
                label="No – people who adhere to antiretroviral treatment (ART) and have a high CD4 count aren’t more at risk "
                value="radio-2"
              ></v-radio>
            </v-radio-group>
          </v-container>
        </v-carousel-item>
        <v-carousel-item>
          <v-container fluid>
            <h1 class="display-2 font-weight-black">
              Should you wear a mask to protect yourself when you go outside?
            </h1>
            <hr />
            <br />
            <v-radio-group class="display-1 font-weight-medium">
              <v-radio
                @click="model++"
                label="Yes – Wear a mask at all times to prevent COVID-19 "
                value="radio-1"
              ></v-radio>
              <v-radio
                @click="response"
                label="No – You don’t need to wear a mask if you’re healthy and not caring for a sick person "
                value="radio-2"
              ></v-radio>
            </v-radio-group>
          </v-container>
        </v-carousel-item>
        <v-carousel-item>
          <v-container fluid>
            <h1 class="display-2 font-weight-black">
              Can COVID-19 be cured?
            </h1>
            <hr />
            <br />
            <v-radio-group class="display-1 font-weight-medium">
              <v-radio
                @click="model++"
                label="Yes – Hot drinks can cure COVID-19 "
                value="radio-1"
              ></v-radio>
              <v-radio
                @click="model++"
                label="No – COVID-19 is a death sentence "
                value="radio-2"
              ></v-radio>
              <v-radio
                @click="response"
                label="No – but most people get better by themselves "
                value="radio-3"
              ></v-radio>
            </v-radio-group>
          </v-container>
        </v-carousel-item>
        <v-carousel-item>
          <v-container fluid>
            <h1 class="display-2 font-weight-black">
              Which of the following is an example of physical distancing?
            </h1>
            <hr />
            <br />
            <v-radio-group class="display-1 font-weight-medium">
              <v-radio
                @click="response"
                label="You stop going to crowded places and visiting other people’s houses "
                value="radio-1"
              ></v-radio>
              <v-radio
                @click="model++"
                label="You stop talking to the people you live with "
                value="radio-2"
              ></v-radio>
              <v-radio
                @click="model++"
                label="You stop speaking to your friends on the phone "
                value="radio-3"
              ></v-radio>
            </v-radio-group>
          </v-container>
        </v-carousel-item>
        <v-carousel-item>
          <v-container fluid>
            <h1 class="display-2 font-weight-black">
              How can people living with HIV protect themselves from COVID-19?
            </h1>
            <hr />
            <br />
            <v-radio-group class="display-1 font-weight-medium">
              <v-radio
                @click="model++"
                label="Wash their hands regularly and follow the physical distancing advice "
                value="radio-1"
              ></v-radio>
              <v-radio
                @click="model++"
                label="Keep taking their antiretroviral treatment "
                value="radio-2"
              ></v-radio>
              <v-radio
                @click="model++"
                label="Exercise regularly, eat well and look after their mental health "
                value="radio-3"
              ></v-radio>
              <v-radio
                @click="response"
                label="All of the above"
                value="radio-4"
              ></v-radio>
            </v-radio-group>
          </v-container>
        </v-carousel-item>
        <v-carousel-item>
          <v-container>
            <h1 class="display-2 font-weight-black text-center">
              Thank you.
            </h1>
            <hr />
            <br />
            <br />
            <br />
            <br />
            <v-row class="fill-height" align="center" justify="center">
              <!-- <img src="~assets/covidscare.jpg" width="900" /> -->

              <v-btn
                outlined
                rounded
                x-large
                color="success"
                class="text-none"
                @click="conclude"
                ><v-icon left>mdi-marker-check</v-icon>Submit your
                responses</v-btn
              >

              <div class="text-center">
                <v-dialog v-model="dialog" width="500">
                  <!-- <template v-slot:activator="{ on }">
        <v-btn
          color="red lighten-2"
          dark
          v-on="on"
        >
          Click Me
        </v-btn>
      </template> -->

                  <v-card>
                    <v-card-title primary-title>
                      Quiz Complete
                    </v-card-title>

                    <v-card-text>
                      You scored {{ this.marks }} out of 10.
                    </v-card-text>

                    <v-divider></v-divider>

                    <v-card-actions>
                      <v-spacer></v-spacer>
                      <v-btn
                        color="primary"
                        text
                        @click="dialog = false"
                        nuxt
                        to="/"
                      >
                        OK
                      </v-btn>
                    </v-card-actions>
                  </v-card>
                </v-dialog>
              </div>
            </v-row>
          </v-container>
        </v-carousel-item>
      </v-carousel>
    </v-tab-item>
  </v-tabs>
</template>

<script>
import VideoPlayer from '@/components/VideoPlayer.vue'
// import vPlayBack from 'v-playback'
export default {
  data() {
    return {
      dialog: false,
      model: 0,
      marks: 0
    }
  },
  components: {
    VideoPlayer
  },
  methods: {
    response() {
      this.$toast.success('Correct Response', {
        iconPack: 'mdi',
        icon: 'mdi-content-save'
      })
      this.marks++
      this.model++
    },
    conclude() {
      // this.$toast.success(
      //   'Quiz completed, you scored ' + this.marks + ' out of 10',
      //   {
      //     iconPack: 'mdi',
      //     icon: 'mdi-content-save'
      //   }
      // )
      this.dialog = true
      // this.model++
    }
  }
}
</script>
<style>
.wall {
  background: url(~assets/cool-background.png) no-repeat center fixed;
  background-size: cover;
}
</style>
