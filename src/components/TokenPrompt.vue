<template>
  <div class="token-prompt">
    <h3>{{ $t('tokenPrompt.title') }}</h3>
    <p>{{ $t('tokenPrompt.intro') }}</p>
    <ol class="login-steps">
      <li>
        <strong>{{ $t('tokenPrompt.step1.title') }}</strong>
        <ol type="a">
          <li>
            {{ $t('tokenPrompt.step1.a.prefix') }}
            <a href="https://go.ifrc.org/account/details" target="_blank" rel="noopener noreferrer">
              {{ $t('tokenPrompt.step1.a.link') }}
            </a>
            {{ $t('tokenPrompt.step1.a.suffix') }}
          </li>
          <li>{{ $t('tokenPrompt.step1.b') }}</li>
          <li>{{ $t('tokenPrompt.step1.c') }}</li>
        </ol>
      </li>
      <li>
        <strong>{{ $t('tokenPrompt.step2') }}</strong>
        <br>
        <button class="btn btn-primary mt-2" @click="$emit('login')">
          {{ $t('tokenPrompt.tokenPromptButton') }}
        </button>
      </li>
    </ol>
  </div>
</template>
<script>
export default {
  name: 'TokenPrompt',
  emits: ['login']
};
</script>
