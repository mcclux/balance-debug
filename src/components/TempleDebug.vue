<template>
    <button @click="connectWallet('temple')">Check Balance</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { TezosToolkit } from '@taquito/taquito';

export default defineComponent({
  name: 'TempleDebug',
  methods: {
    async connectWallet (wtype: string) {
      if (wtype === 'temple') {
        const tezos = new TezosToolkit('https://rpc.tzstats.com');
        const balance = tezos.tz.getBalance('tz1a8QSHVHVkCmDYio6ptk7LAL7ZvywL6Vjo')
      }
    }
  }
})
</script>