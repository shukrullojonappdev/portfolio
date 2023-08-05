<script setup lang="ts">
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Tushunuvchanlik</template>
    Boshqalar kodini tushunish, dokumenttatsiyalarni o'qib ishlata olish, tushunarli kod yozish.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Ish qurollar</template>
    Visual Studio Code, Chrome Dev Tools, Angular Dev Tools, Redux Dev Tools, Vue Dev Tools,
    Powershell, Bash, Linux, Windows.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Ekosistema</template>
    <strong>Backend:</strong> nestjs, mysql, sqlite, supabase, firebase ...
    <br />
    <strong>Frontend:</strong> angular, vue, redux, pinia, formkit, angular forms ...
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Kelishuvchanlik</template>

    Yangi odamlar bilan yaxshi kelishaman. Ona tilim o'zbek tili, rus tilida erkin gaplasha olaman,
    ingliz tilim o'rtacha.
  </WelcomeItem>
</template>
