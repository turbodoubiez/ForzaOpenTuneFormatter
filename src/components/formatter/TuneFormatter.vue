<script setup lang="ts">
import { useFormattingFormProvider } from '../../lib/useFormattingForm';
import BuildSettingsForm from './BuildSettingsForm.vue';
import TuneSettingsForm from './TuneSettingsForm.vue';
import GlobalUnitSelect from '../GlobalUnitSelect.vue';
import FormattedTuneTextarea from './FormattedTuneTextarea.vue';
import CarStatsForm from './CarStatsForm.vue';
import ShareCodesForm from './ShareCodesForm.vue';

const {
  form,
  globalUnit,
} = useFormattingFormProvider();

</script>

<template>
  <h1>TUNE FORMATTER</h1>
  <p class="sub-title">
    Create and share your tune.
    This tool will automatically create an easy-to-read
    format you can share on our subreddit.
  </p>
  <div class="flex flex-col md:flex-row items-start">
    <form class="grow">
      <GlobalUnitSelect v-model="globalUnit" />
      <CarStatsForm />
      <ShareCodesForm />
      <BuildSettingsForm />
      <TuneSettingsForm />
    </form>
    <FormattedTuneTextarea />
  </div>
</template>
