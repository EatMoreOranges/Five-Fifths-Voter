<template>
  <PageLayout childData="mother-daughter-hero.jpeg">
    <div class="page__details">
      <h2 class="page__title">{{ $t('why_vote_page.header') }}</h2>
    </div>
    <MainContent>
      <template v-slot:content>
        <aside class="aside">
          <div class="aside__container--text">
            <h2 class="aside__header">{{ $t('why_vote_page.title') }}</h2>
            <p class="aside__paragraph">
              {{ $t('why_vote_page.paragraph1') }}
              <br /><br />
              {{ $t('why_vote_page.paragraph2') }}
              <br /><br />
              {{ $t('why_vote_page.paragraph3') }}
              <br /><br />
              {{ $t('why_vote_page.final_sentence_part1') }}
              <strong
                ><em>{{ $t('why_vote_page.final_sentence_part2') }}</em></strong
              >,
              <strong
                ><em>{{ $t('why_vote_page.final_sentence_part3') }}</em></strong
              >,
              <strong
                ><em>{{ $t('why_vote_page.final_sentence_part4') }}</em></strong
              >, {{ $t('why_vote_page.final_sentence_part5') }}
              <strong
                ><em>{{ $t('why_vote_page.final_sentence_part6') }}</em></strong
              >.
            </p>
          </div>
        </aside>
      </template>
      <template v-slot:image>
        <aside class="aside__container--img">
          <img
            class="aside__image"
            src="../../assets/why-vote-page-father-daughter-image-1.jpg"
            alt="A young father holds his infant daughter on his shoulders"
          />
        </aside>
      </template>
    </MainContent>
  </PageLayout>
</template>

<script>
import PageLayout from '../../components/PageLayout';
import MainContent from '../../components/MainContent';

export default {
  name: 'connect',
  components: { PageLayout, MainContent },
  data() {
    return {};
  },
  created() {
    this.$amplitude.getInstance().logEvent('Page Visit', { page: 'Why Vote Page' });
  },
  methods: {}
};
</script>
