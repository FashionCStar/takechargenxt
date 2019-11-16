<template>
  <q-layout view="lHh lpr lFf" class="shadow-2 rounded-borders">
      <q-header bordered class="bg-white text-primary">
        <q-toolbar>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo/svg/quasar-logo.svg">
          </q-avatar>

          <q-toolbar-title></q-toolbar-title>

          <q-btn outline color="teal-10">Login</q-btn>
        </q-toolbar>
      </q-header>
      <div class="column">
        <div id="homeBanner">
          <div class="row q-mx-xl">
            <div class="col-12 col-md-6 column justify-center items-center">
              <div class="text-center">
                <h2 class="text-white q-px-xl q-my-none">Put cash back in your wallet!</h2>
                <q-btn round class="shadow-10 q-my-xl" size="30px">
                  <q-avatar size="90px">
                    <q-icon name="play_circle_outline" color="white" size="90px"></q-icon>
                  </q-avatar>
                </q-btn>
                <p class="text-white text-h5">See how in 43 seconds</p>
              </div>
            </div>
            <div class="col-12 col-md-6 column justify-center items-center">
              <div style="max-width: 400px;" class="full-width text-center">
                <q-form
                  class="q-gutter-md bg-white full-width rounded-borders q-pa-md"
                >
                  <div class="text-center" style="font-size: 28px">Join for free!!!</div>
                  <q-input outlined color="teal-10" v-model="userData.email" clearable label="Email Address" class="q-ml-none">
                    <template v-slot:prepend>
                      <q-icon name="account_circle" />
                    </template>
                  </q-input>
                  <q-input outlined color="teal-10" label="Password" v-model="userData.password" clearable class="q-ml-none">
                    <template v-slot:prepend>
                      <q-icon name="lock" />
                    </template>
                  </q-input>
                  <q-input outlined color="teal-10" label="Confirm Password" v-model="userData.confirm" clearable class="q-ml-none">
                    <template v-slot:prepend>
                      <q-icon name="lock" />
                    </template>
                  </q-input>

                  <q-input outlined color="teal-10" label="Enter sign up code" clearable class="q-ml-none">
                    <template v-slot:prepend>
                      <q-icon name=" " />
                    </template>
                  </q-input>
                  <q-btn type="submit" class="full-width bg-cyan-7 text-white">
                    Sign Up Now
                  </q-btn>
                  <div class="row">
                    <div class="col-5">
                      <q-linear-progress :value="0" size="1px" class="q-mt-sm" />
                    </div>
                    <div class="col-2 text-center">
                      <span>or</span>
                    </div>
                    <div class="col-5">
                      <q-linear-progress :value="0" size="1px" class="q-mt-sm" />
                    </div>
                  </div>
                  <q-btn class="full-width text-white" style="background-color:#3b5998">Sign up with Facebook</q-btn>
                  <!--<q-toggle v-model="accept" label="By clicking here I agree to receive periodic emails with offers and promotional marketing messages from Swagbucks." />-->
                  <q-item tag="label" class="q-ma-none q-pa-none q-mt-lg">
                    <q-item-section avatar>
                      <q-toggle color="red" v-model="accept"/>
                    </q-item-section>
                    <q-item-section>
                      <q-item-label caption>By clicking here I agree to receive periodic emails with offers and promotional marketing messages from Swagbucks.</q-item-label>
                    </q-item-section>
                  </q-item>
                </q-form>
                <div class="q-mt-4 text-white">By Signing up I agree to the Terms and Privacy Policy.</div>
              </div>
            </div>
          </div>
        </div>
        <div class="bg-blue-grey-1" style="border-bottom: .1rem solid #d2d7da;">
          <div class="row q-px-xl q-py-lg q-mx-xl items-center">
            <div class="col-12 col-sm-2">
              <span style="font-size: 16px">As seen on</span>
            </div>
            <div class="col-12 col-sm-2">
              <q-img style="height: 60px" contain src="https://app6-cdn2.sbx-cdn.com/content/home-6/images/logged-out/logos/logo-buzzfeed.svg?v=8041930-071a"></q-img>
            </div>
            <div class="col-12 col-sm-2">
              <q-img style="height: 60px" contain src="https://app6-cdn2.sbx-cdn.com/content/home-6/images/logged-out/logos/logo-save-the-student.svg?v=8041930-cafa"></q-img>
            </div>
            <div class="col-12 col-sm-2">
              <q-img style="height: 60px" contain src="https://app6-cdn2.sbx-cdn.com/content/home-6/images/logged-out/logos/logo-the-penny-hoarder.svg?v=8041930-3c3a"></q-img>
            </div>
            <div class="col-12 col-sm-2">
              <q-img style="height: 60px" contain src="https://app6-cdn2.sbx-cdn.com/content/home-6/images/logged-out/logos/logo-abc.svg?v=8041930-d29a"></q-img>
            </div>
            <div class="col-12 col-sm-2">
              <q-img style="height: 60px" contain src="https://app6-cdn2.sbx-cdn.com/content/home-6/images/logged-out/logos/logo-huffington-post.svg?v=8041930-071a"></q-img>
            </div>
          </div>
        </div>
        <div>
          <div class="q-px-xl q-py-lg q-mx-xl items-center">
            <div class="text-center">
              <span class="text-h3 text-weight-light">Get <strong>Free</strong> Gift Cards &amp; Cash for the everyday things you do online. Here's how…</span>
            </div>
            <div class="row q-mt-xl">
              <div style="max-width: 500px" class="col-12 col-md-5 text-center q-mx-auto">
                <img style="height: 90px; width: 300px" src="../assets/images/icon-set1.png" />
                <h2>End Points</h2>
                <p class="text-h5">Shop online, Watch entertaining videos, Search the web, Answer
                  surveys and find great deals to earn your points.</p>
              </div>
              <div class="col-12 col-md-2 items-center justify-center" style="display: flex">
                <img src="../assets/images/arrow-right.png" />
              </div>
              <div style="max-width: 500px" class="col-12 col-md-5 text-center q-mx-auto">
                <q-img style="height: 90px; width: 300px" src="https://app6-cdn2.sbx-cdn.com/content/home-6/images/logged-out/gift-cards-UK.min.svg" />
                <h2>Get Free Gift Cards</h2>
                <p class="text-h5">Redeem your points for gift cards to your favorite retailers like Amazon and Walmart or get cash back from PayPal.</p>
              </div>
            </div>
          </div>
        </div>
        <div class="bg-blue-grey-1" style="border-bottom: .1rem solid #d2d7da;">
          <div class="q-px-lg q-mx-xl items-center text-center" style="padding-top: 60px; padding-bottom: 50px;">
            <div class="text-h2 q-pb-lg">We’ve paid our members over</div>
            <div id="flipCounterWrapper">
              £
              <div id="flipCounter">
                <span class="flipCounterFrame">
                  <span class="flipCounterDigit">2</span>
                </span>
                <span class="flipCounterFrame">
                  <span class="flipCounterDigit">3</span>
                </span>
                <span class="flipCounterFrame">
                  <span class="flipCounterDigit">0</span>
                </span>
                ,
                <span class="flipCounterFrame">
                  <span class="flipCounterDigit">9</span>
                </span>
                <span class="flipCounterFrame">
                  <span class="flipCounterDigit">7</span>
                </span>
                <span class="flipCounterFrame">
                  <span class="flipCounterDigit">5</span>
                </span>
                ,
                <span class="flipCounterFrame">
                  <span class="flipCounterDigit">0</span>
                </span>
                <span class="flipCounterFrame">
                  <span class="flipCounterDigit">4</span>
                </span>
                <span class="flipCounterFrame">
                  <span class="flipCounterDigit">2</span>
                </span>
              </div>
            </div>
          </div>
        </div>
        <div>
          <div class="q-px-xl q-py-lg q-mx-xl items-center" style="display: flex; max-width: 800px; margin: auto">
            <q-avatar class="q-ma-lg" size="90px">
              <q-img src="https://app6-cdn2.sbx-cdn.com/content/home-6/images/logged-out/testimonials/female-mid3.jpg"></q-img>
            </q-avatar>
            <p class="text-left testimonial">
              “My most rewarding moment with Swagbucks is using the gift cards I earn to buy gifts for my child's Christmas and February birthday.”
              <span class="testimonialMeta">
                <span class="testimonialMetaName">Kim,</span>
                Member since 2009
              </span>
            </p>
          </div>
        </div>
        <div class="bg-blue-grey-1" style="border-bottom: .1rem solid #d2d7da;">
          <div class="q-px-lg q-mx-xl q-py-xl items-center text-center" >
            <div class="row">
              <div class="col-2"></div>
              <div class="col-3">
                <q-linear-progress :value="0" size="2px" class="q-mt-lg" />
              </div>
              <div class="col-2 text-center">
                <img src="../assets/images/horizontal-line.png" />
              </div>
              <div class="col-3">
                <q-linear-progress :value="0" size="2px" class="q-mt-lg" />
              </div>
              <div class="col-2"></div>
            </div>
            <p id="lpContentGcCopy">
              We give out <strong>7,000</strong> free gift cards <em>every day</em>
            </p>
          </div>
        </div>
      </div>
  </q-layout>
</template>

<style>
  #flipCounterWrapper {
    font-family: 'Open Sans',sans-serif;
    font-size: 4.5em;
    line-height: 1.462;
    font-weight: 500;
    color: #6bb0c6;
    text-align: center;
  }
  #flipCounter {
    display: inline-block;
    position: relative;
    background-color: #2e8da9;
    border-radius: .123em;
    color: #fff;
    line-height: 1;
    padding: .277em;
    vertical-align: bottom;
    margin-left: .108em;
  }
  .flipCounterFrame {
    position: relative;
    display: inline-block;
    height: 1.08em;
    width: .8em;
    border-radius: .123em;
    margin: 0 .0385em;
    background-color: #89cddc;
    overflow: hidden;
    vertical-align: middle;
  }
  .flipCounterFrame:before {
     content: '';
     position: absolute;
     top: .0154em;
     left: 0;
     width: 100%;
     height: .54em;
     background-color: #6bb0c6;
     z-index: 0;
     border-top-left-radius: .1385em;
     border-top-right-radius: .1385em;
  }
  .flipCounterDigit {
    position: relative;
    z-index: 1;
    line-height: 1;
  }
  .flipCounterDigit:before {
    content: '';
    position: absolute;
    top: -.17em;
    bottom: 0;
    left: 100%;
    height: .0155em;
    width: 300%;
    margin: auto;
    background-color: #5fa3b8;
    box-sizing: border-box;
    z-index: 2;
  }
  .flipCounterDigit:after {
    content: '';
    position: absolute;
    top: .05em;
    bottom: 0;
    left: -100%;
    height: .0155em;
    width: 300%;
    margin: auto;
    background-color: #85cde5;
    box-sizing: border-box;
    z-index: 2;
  }
  .flipCounterFrame:after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: .54em;
    background-color: #5fa3b8;
    z-index: 0;
  }
  .testimonial {
    font-size: 24px;
    font-weight: 400;
    line-height: 1.36;
    color: #2b2a26;
    overflow: auto;
    margin: 0;
    display: inline-block;
    vertical-align: middle;
  }
  .testimonialMeta {
    display: block;
    font-size: .56em;
    color: #999;
    margin-top: .7rem;
  }
  .testimonialMetaName {
    font-size: 1.43em;
    color: #666;
  }
  #lpContentGcCopy {
    font-size: 2em;
    line-height: 1.2;
    color: #666;
  }
  #lpContentGcCopy strong {
    font-size: 2.25em;
    color: #6ec9c0;
    font-weight: 300;
    vertical-align: middle;
    padding: 0 .5rem;
  }
</style>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      color: 'primary',
      response: '',
      loading: false,
      userData: {
        email: '',
        password: '',
        confirm: ''
      },
      accept: false
    }
  },
  created () {
    console.log('hey index.vue')
  },
  methods: {
    // async makeRequest () {
    //   let response
    //   let color = 'negative'
    //   this.loading = true

    //   try {
    //     response = ''
    //     let req = await fetch(process.env.api + '/test')

    //     if (!req.ok) throw new Error('error request')

    //     let {data} = await req.json()
    //     response = data
    //     color = 'positive'
    //   } catch (err) {
    //     console.log(err)
    //     response = err.message
    //   }

    //   setTimeout(() => {
    //     this.response = response
    //     this.color = color
    //     this.loading = false
    //   }, 700)
    // }
    makeRequest () {
      //   let response
      //   let color = 'negative'
      this.loading = true
      this.$axios
        .get('/test')
        .then(res => {
          console.log('res', res)
          this.loading = false
        })
        .catch(err => {
          this.loading = false
          console.log('err', err)
        })

      //   try {
      //     response = ''
      //     let req = await fetch(process.env.api + '/test')

      //     if (!req.ok) throw new Error('error request')

      //     let {data} = await req.json()
      //     response = data
      //     color = 'positive'
      //   } catch (err) {
      //     console.log(err)
      //     response = err.message
      //   }

      //   setTimeout(() => {
      //     this.response = response
      //     this.color = color
      //     this.loading = false
      //   }, 700)
    }
  }
}
</script>
