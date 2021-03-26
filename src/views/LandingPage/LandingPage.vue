<template>
  <PageLayout childData="mother-daughter-hero.jpeg">
    <Countdown />
    <MainContent>
      <template v-slot:content>
        <article class="article">
          <div class="article__content">
            <h2 class="article__heading">{{ $t('landing_page.mission.title') }}</h2>
            <div class="bx--offset-lg-1">
              <p class="article__paragraph">
                {{ $t('landing_page.mission.paragrah') }}
              </p>
            </div>
          </div>
        </article>
      </template>
      <template v-slot:image>
        <div class="article__img-container">
          <img
            class="article__img"
            src="../../assets/landing-page-man-on-laptop-image-1.jpg"
            alt="Man lounges on beanbag chair while browsing on his laptop"
          />
        </div>
      </template>
    </MainContent>
    <MainContent>
      <template v-slot:content>
        <article class="article">
          <div class="article__content">
            <h2 class="article__heading">{{ $t('landing_page.educate.title') }}</h2>
            <span class="article__quote"
              >&quot;{{ $t('landing_page.educate.quote') }}&quot;<span class="quote--author"
                >- {{ $t('landing_page.educate.author') }}</span
              ></span
            ><br /><br />
            <div class="bx--offset-lg-1">
              <p class="article__paragraph">
                {{ $t('landing_page.educate.paragraph') }}
              </p>
            </div>
          </div>
        </article>
      </template>
      <template v-slot:image>
        <div class="article__img-container">
          <img
            class="article__img"
            src="../../assets/landing-page-grandpa-grandson-image-2.jpeg"
            alt="A smiling grandfather dotes on his baby grandson that he's holding"
          />
        </div>
      </template>
    </MainContent>
    <MainContent>
      <template v-slot:content>
        <article class="article">
          <div class="article__content">
            <h2 class="article__heading">{{ $t('landing_page.empower.title') }}</h2>
            <span class="article__quote"
              >&quot;{{ $t('landing_page.empower.quote') }} &quot;
              <span class="quote--author">- {{ $t('landing_page.empower.author') }}</span></span
            ><br /><br />
            <div class="bx--offset-lg-1">
              <p class="article__paragraph">
                {{ $t('landing_page.empower.paragraph') }}
              </p>
            </div>
          </div>
        </article>
      </template>
      <template v-slot:image>
        <div class="article__img-container">
          <img
            class="article__img"
            src="../../assets/landing-page-black-woman-orange-image-3.jpeg"
            alt="Black woman wearing bright orange against brick wall smiles into distance"
          />
        </div>
      </template>
    </MainContent>
    <MainContent>
      <template v-slot:content>
        <article class="article">
          <div class="article__content">
            <h2 class="article__heading">{{ $t('landing_page.enable.title') }}</h2>
            <span class="article__quote"
              >&quot;{{ $t('landing_page.enable.quote') }} &quot;
              <span class="quote--author">- {{ $t('landing_page.enable.author') }}</span></span
            ><br /><br />
            <div class="bx--offset-lg-1">
              <p class="article__paragraph">
                {{ $t('landing_page.enable.paragraph') }}
              </p>
            </div>
          </div>
        </article>
      </template>
      <template v-slot:image>
        <div class="article__img-container">
          <img
            class="article__img"
            src="../../assets/landing-page-disabled-triathlete-image-4.jpeg"
            alt="A young teenaged paraplegic is racing in a wheelchair"
          />
        </div>
      </template>
    </MainContent>
  </PageLayout>
</template>

<script>
import Countdown from '../../components/Countdown';
import PageLayout from '../../components/PageLayout';
import MainContent from '../../components/MainContent';

export default {
  name: 'LandingPage',
  props: {
    heroImage: String
  },
  components: { Countdown, PageLayout, MainContent },
  data() {
    return {
      yourName: '',
      firstName: '',
      lastName: '',
      dob: '',
      visible: false
    };
  },
  created() {
    this.$amplitude.getInstance().logEvent('Page Visit', { page: 'Landing Page' });
  },
  methods: {
    onClick() {
      this.visible = true;
    },
    modalClosed() {
      this.visible = false;
    }
  }
};
</script>

<style lang="scss">
@import './landingpage.scss';
</style>
