<template>
  <div class="container">
    <CThemeProvider>
      <CColorModeProvider>
        <CBox
          font-family="body"
          as="main"
          class="layout-wrapper"
        >
          <CReset />
          <div class="nuxt-content">
            <Nuxt />
          </div>
          <app-toolbar />
        </CBox>
      </CColorModeProvider>
    </CThemeProvider>
  </div>
</template>
<script>
import {
  CThemeProvider,
  CColorModeProvider,
  CReset,
  CBox,
} from '@chakra-ui/vue';
import AppToolbar from '@/components/AppToolbar.vue';

export default {
  name: 'DefaultLayout',
  components: {
    AppToolbar,
    CThemeProvider,
    CColorModeProvider,
    CReset,
    CBox,
  },
  middleware: ['auth', 'hasPet'],
};
</script>
