<template>
  <div class="home loading" @click="start">
    <Header title="Home" :decorate="false"></Header>
    <Awards></Awards>
    <HomeBanner></HomeBanner>
    <Transition name="fade">
      <div class="device-tips-wrap" v-if="deviceTipsActive">
        <div class="device-tips">
          <div class="img-wrap">
            <img
              src="https://static.igem.wiki/teams/4774/wiki/static/svg/chrome.svg"
              alt=""
            />
          </div>
          <div class="text">
            We recommend using <b>Chrome</b> on your <b>laptop</b> for best effect
          </div>
        </div>
      </div>
    </Transition>
    <PageIndexMap ref="map" />
    <div class="section" data-scrollent="fade-up">
      <div class="text-box">
        <p class="line middle">
          Lung cancer is a malignant tumor that
          <b>originated in the lungs</b> and may spread to lymph nodes or other
          surrounding organs in the body. It can be categorized into two main
          types:
        </p>
        <p class="line large"><b>Non-Small Cell Lung Carcinoma (NSCLC)</b></p>
        <p class="line middle">Small Cell Lung Carcinoma (SCLC)</p>
        <img
          class="text-box-img img-lung"
          src="https://static.igem.wiki/teams/4774/wiki/static/svg/home/lung.svg"
          data-scrollent="fade-left"
          data-scrollent-delay="200"
          data-scrollent-distance="100%"
          data-scrollent-duration="1000"
        />
      </div>
    </div>
    <div class="section world">
      <div class="text-wrap">
        <p
          class="line very-large"
          data-scrollent-ref=".section.world"
          data-scrollent="fade-left"
          data-scrollent-delay="100"
          data-scrollent-percent="0.4"
        >
          Lung cancer
        </p>
        <p
          class="line"
          data-scrollent-ref=".section.world"
          data-scrollent="fade-left"
          data-scrollent-delay="200"
          data-scrollent-percent="0.4"
        >
          The <span class="large">2nd</span> common cancer worldwide
        </p>
        <p
          class="line"
          data-scrollent-ref=".section.world"
          data-scrollent="fade-left"
          data-scrollent-delay="400"
          data-scrollent-percent="0.4"
        >
          <span class="large">Leading cause</span> of cancer-related mortalities
          worldwide
        </p>
        <p
          class="line"
          data-scrollent-ref=".section.world"
          data-scrollent="fade-left"
          data-scrollent-delay="500"
          data-scrollent-percent="0.4"
        >
          Commonly diagnosed at <span class="large">advanced stages</span> with
          limited treatment options
        </p>
      </div>
      <PageIndexEarth
        class="earth"
        data-scrollent-ref=".section.world"
        data-scrollent="fade-left"
        data-scrollent-percent="0.3"
      />
    </div>
    <div class="section">
      <div class="text-box">
        <p class="line very-large">Osimertinib</p>
        <p class="line middle indent-left-1">
          The current
          <span class="large"><b>first-line treatment</b></span> used to treat
          patients with advanced-stage NSCLC.
        </p>
        <p class="line middle indent-left-1">
          Third generation epidermal growth factor receptor (EGFR) tyrosine
          kinase inhibitor (TKI).
        </p>
        <p class="line middle indent-left-1">
          Specified for NSCLC patients with EGFR T790M mutation.
        </p>
        <img
          class="text-box-img img-lung"
          src="https://static.igem.wiki/teams/4774/wiki/static/svg/home/osimertinib.svg"
          data-scrollent="fade-left"
          data-scrollent-delay="200"
          data-scrollent-distance="100%"
          data-scrollent-duration="1000"
        />
      </div>
    </div>
    <div class="section half-page page-bottom">
      <div class="full-page-wrap">
        <div class="line font-hHeliuma s-70 center highlight">However</div>
        <p class="line middle center mt-20">
          Osimertinib <span class="large"><b>Resistance</b></span> Inevitably
          Develops Among NSCLC Patients
        </p>
      </div>
    </div>
    <div class="section">
      <div class="text-box">
        <p class="line very-large">Osimertinib resistance</p>
        <p class="line middle indent-left-1">
          Develops in EGFR T790M mutation-positive NSCLC patients
        </p>
        <p class="line middle indent-left-1">
          Osimertinib is no longer able to halt the growth of NSCLC tumor
        </p>
        <img class="text-box-img img-lung" src="" />
      </div>
    </div>
    <div class="section full-page page-bottom however">
      <div class="section-content">
        <p class="line very-large center fc-main">
          <b>Nonetheless, the story doesn’t conclude here!</b>
        </p>
        <Horizontal left="70%">
          <p class="line large">
            We, <b>PolYneer</b>, are committed to developing a
            <b>novel bispecific antibody</b> using a synthetic biology approach
            to address the unmet clinical need for new agent to overcome
            Osimertinib resistance in NSCLC patients.
          </p>
          <template v-slot:right>
            <div class="polyneerab-wrap">
              <div class="lottie-wrap">
                <Lottie
                  animationLink="https://static.igem.wiki/teams/4774/wiki/static/json/pages/home/home-polyneerab.json"
                />
              </div>
              <p class="polyneerab-text">Polyneerab</p>
            </div>
          </template>
        </Horizontal>
      </div>
    </div>
    <div class="section">
      <PageIndexAbIntro class="ab-intro" />
    </div>
    <div class="section comparison">
      <div class="antibody-wrap">
        <Horizontal left="30%">
          <img
            class="antibody-img"
            src="https://static.igem.wiki/teams/4774/wiki/static/img/home/traditional-2.png"
            alt=""
          />
          <template v-slot:right>
            <div class="antibody-text">
              <p class="antibody">
                Traditional bispecific antibody production (e.g. amivantamab)
                relies on the co-culture of two different cell types expressing
                half of the light-heavy chain of the antibody, and the
                subsequent dimerization of the half antibody secreted by the two
                cell types.
              </p>
              <p class="line large">
                Due to the complicated production process:
              </p>
              <List
                :serial="false"
                :data="[
                  'The therapy cost of traditional bispecific antibody is <b>very high</b>',
                  'Ranging from USD 30,000 to USD 170,000 per treatment, which is barely affordable to most patients',
                ]"
              />
            </div>
          </template>
        </Horizontal>
      </div>
      <div class="antibody-wrap">
        <Horizontal left="30%">
          <img
            class="antibody-img"
            src="https://static.igem.wiki/teams/4774/wiki/static/img/home/novel-2.png"
            alt=""
          />
          <template v-slot:right>
            <div class="antibody-text">
              <p class="line large"><b>Advantages</b> of Polyneerab</p>
              <List
                :serial="false"
                :data="[
                  'Flexible design',
                  'Lower production cost',
                  'Rapid production',
                  'More stable structure and intact Fab conformation as no protein refolding is involved',
                ]"
              />
            </div>
          </template>
        </Horizontal>
      </div>
    </div>
    <div class="section">
      <Horizontal class="polyneerab-treat" left="40%">
        <p class="line large">
          With Polyneerab in combination with Osimertinib, we believe that we
          can give renewed hope to NSCLC patients!!
        </p>
        <template v-slot:right>
          <div class="lottie-wrap">
            <Lottie
              animationLink="https://static.igem.wiki/teams/4774/wiki/static/json/pages/home/home-treat.json"
            />
          </div>
        </template>
      </Horizontal>
    </div>
    <div class="section">
      <div class="sub-title font-hHeliuma">Our Promotion Video</div>
      <iframe
        class="video"
        title="HKPOLYU: Polyneerab-Novel Bi-specific Antibody (2023) - Project Promotion [English]"
        width="560"
        height="315"
        src="https://video.igem.org/videos/embed/9864bb11-5b9b-43eb-89d0-33a0be039480?subtitle=en"
        frameborder="0"
        allowfullscreen=""
        sandbox="allow-same-origin allow-scripts allow-popups"
      ></iframe>
      <p class="line large center">
        <b
          >To learn more details about our project, you can visit our specific
          pages</b
        >
      </p>
      <div class="page-card-wrap">
        <PageCard url="/hkpolyu/description"> Description </PageCard>
        <PageCard
          url="/hkpolyu/results"
          img-url="https://static.igem.wiki/teams/4774/wiki/static/svg/pages/results.svg"
        >
          Results
        </PageCard>
        <PageCard
          url="/hkpolyu/human-practices"
          img-url="https://static.igem.wiki/teams/4774/wiki/static/img/ihp/ihp.png"
        >
          Human Practices
        </PageCard>
        <PageCard
          url="/hkpolyu/entrepreneurship"
          img-url="https://static.igem.wiki/teams/4774/wiki/static/svg/pages/entrepreneurship-2.svg"
        >
          Entrepreneurship
        </PageCard>
        <PageCard
          url="/hkpolyu/judging"
          img-url="https://static.igem.wiki/teams/4774/wiki/static/svg/pages/judging.svg"
        >
          Judging
        </PageCard>
      </div>
    </div>
    <div class="donators">
      <div class="sub-title font-hHeliuma">Our Sponsors</div>
      <div class="donator-wrap">
        <div class="donator">
          <a href="https://sg.idtdna.com/" target="_blank">
            <img
              class="donator-logo"
              src="https://static.igem.wiki/teams/4774/wiki/static/svg/home/logo-idt.svg"
            />
          </a>
        </div>
        <div class="donator">
          <a href="https://www.snapgene.com/" target="_blank">
            <img
              class="donator-logo"
              src="https://static.igem.wiki/teams/4774/wiki/static/svg/home/logo-snapgene.svg"
            />
          </a>
        </div>
        <div class="donator">
          <a href="http://www.synpeptide.com/" target="_blank">
            <img
              class="donator-logo"
              src="https://static.igem.wiki/teams/4774/wiki/static/img/home/logo-synpeptide.png"
            />
          </a>
        </div>
        <div class="donator">
          <a href="https://www.beckmancoulter.com/en" target="_blank">
            <img
              class="donator-logo"
              src="https://static.igem.wiki/teams/4774/wiki/static/svg/home/logo-beckman.svg"
            />
          </a>
        </div>
      </div>
    </div>
    <div class="section">
      <img
        class="img-pioneering"
        src="https://static.igem.wiki/teams/4774/wiki/static/img/home/pioneering-the-future.png"
        alt=""
      />
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    const { $Scrollent } = useNuxtApp();
    return {
      $Scrollent,
    };
  },
  data() {
    const deviceTipsActive = false;
    return {
      deviceTipsActive,
    };
  },
  mounted() {
    utils.lockScroll();
    let isChrome = false;
    let userAgent = navigator.userAgent.toLowerCase();
    if (/chrome/i.test(userAgent)) {
      isChrome = true;
    }
    if (!isChrome) {
      this.deviceTipsActive = true;
      setTimeout(() => {
        this.deviceTipsActive = false;
      }, 4000);
    }
  },
  methods: {
    start() {
      console.log("start");
      this.$refs.map.playStartingAnimation();
    },
  },
};
</script>
<style lang="scss" scroped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

iframe {
  margin: 20px auto;
}

.device-tips-wrap {
  position: fixed;
  display: flex;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 20px;
  align-items: center;
  justify-content: center;
  pointer-events: none;
  z-index: 999999999;

  .device-tips {
    text-align: center;
    background-color: rgba(0, 0, 0, 0.6);
    padding: 10px 20px;
    border-radius: 20px;
    color: #fff;
    font-size: 1.5em;

    .img-wrap {
      width: 20vw;
      margin: 10px auto;
      opacity: 0.9;
    }

    @media (max-width: 991px) {
      .img-wrap {
        width: 60vw;
      }
    }
  }
}

.home {
  padding-top: 0;
  margin-top: 0;
  background-image: linear-gradient(to top, #a8edea 0%, $main-a2 100vh);
}

.section {
  position: relative;
  width: 100vw;
  padding-top: 56px;
  padding: 20px 10vw;
  font-size: 24px;

  &.full-page,
  &.half-page,
  &.three-quarters-page {
    height: 50vh;
    display: flex;
    flex-direction: column;
    justify-content: center;

    &.page-bottom {
      justify-content: flex-end;
    }
  }

  &.three-quarters-page {
    height: 75vh;
  }

  &.full-page {
    height: 100vh;
  }

  .line {
    line-height: 1em;
    margin-bottom: 0.5em;
    text-align: justify;

    &.highlight {
      color: $main-mid-dark;
    }

    &.s-70 {
      font-size: 70px;
      margin-bottom: 0;
    }

    &.fc-main,
    .fc-main {
      color: $main-color;
    }

    &.mt-20 {
      margin-top: 20px;
    }

    &.center {
      text-align: center;
    }

    &.indent-left-1 {
      margin-left: 1em;
    }

    &.very-large,
    .very-large {
      font-size: 1.8em;
      line-height: 1.4em;
      margin-bottom: 0.5em;
    }

    &.large,
    .large {
      font-size: 1.3em;
      line-height: 1.3em;
    }

    &.middle,
    .middle {
      font-size: 1.1em;
      line-height: 1.4em;
    }

    &.small {
      font-size: 0.8em;
      line-height: 1em;
    }
  }

  .text-box {
    position: relative;
    width: 90%;
    margin: 10px auto;
    background-color: $main-very-light;
    box-shadow: $shadow-1;
    border-radius: 10px;
    padding: 10px 20px;
    overflow: hidden;

    .text-box-img {
      position: absolute;
      width: 20%;
      right: -10px;
      bottom: -20px;
      opacity: 0.4;
    }
  }
}

.section {
  &.world {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-end;
    padding-right: 36vw;

    p {
      text-align: right;
    }

    .earth {
      position: absolute;
      top: 0;
      height: 100%;
      right: -40vw;
    }
  }

  &.comparison {
    .antibody-wrap {
      margin: 100px 0;
    }

    .antibody-img {
      width: 90%;
      margin: 10px;
    }

    .antibody-text {
      margin-left: 10px;
      text-align: justify;

      .antibody {
        font-size: 0.9em;
        line-height: 1.5em;
        margin-bottom: 0.5em;
      }
    }
  }

  .img-pioneering {
    width: 50%;
    margin: 0 auto 100px auto;
  }

  .polyneerab-treat {
    width: 80%;
    margin: 0 auto;
  }

  .ab-intro {
    margin: 0 auto;
  }
}

.polyneerab-wrap {
  text-align: center;
  height: 250px;

  .lottie-wrap {
    height: 200px;
  }
}

.section-blank {
  height: 100vh;
}

.donators {
  font-size: 40px;
}

.donator-wrap {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  flex-direction: row;
  margin: 0 10%;
  padding-bottom: 60px;
}

.donator {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 20%;
  padding: 20px;
}

.donator img {
  width: 100%;
  height: auto;
}

.sub-title {
  position: relative;
  text-align: center;
  margin: 40px auto 20px auto;
  z-index: 10;
  font-size: 70px;
  width: fit-content;

  &::after {
    background-color: $main-mid;
    content: "";
    height: 10px;
    width: 90%;
    display: block;
    position: relative;
    top: -16px;
    z-index: -1;
    margin: 0 auto;
    text-align: center;
  }
}

@media (max-width: 991px) {
  .sub-title {
    font-size: 40px;
    line-height: 40px;
  }

  .page-card {
    img {
      width: 100%;
    }
  }

  .donator-wrap {
    width: 100vw;
    padding: 0 10px 60px 10px;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    margin: 0;
  }
  .donator {
    width: 45%;
    padding: 10px;
  }

  .img-pioneering {
    width: 100% !important;
  }

  .text-box {
    .text-box-img {
      width: 50% !important;
    }
  }

  .section {
    .line {
      &.very-large,
      .very-large {
        * {
          font-size: 1.3em;
          line-height: 1.3em;
        }
      }
    }
    &.world {
      position: relative;
      top: 0;
      height: 100vh;
      width: 100vw;
      display: block;
      padding-right: 40px;
      padding-top: 10vh;
      z-index: 99;

      .text-wrap {
        margin-top: 10vh;
      }

      .earth {
        position: absolute;
        top: 0;
        height: 100%;
        right: -120vw;
        width: 200vw;
        opacity: 0.5;
      }
    }
  }
}
</style>

