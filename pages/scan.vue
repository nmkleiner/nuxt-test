<script setup lang="ts">
import {QrcodeStream} from 'vue-qrcode-reader';

const stopCamera = ref(false);

const onDecode = (result: string) => {
  alert(result);
  stopCamera.value = true;
};
</script>

<template>
<h1>scan</h1>

  <QrcodeStream
    :debug="false"
    :stop="stopCamera"
    @decode="onDecode"
    style="width: 100%;"
  />
</template>

<style scoped>

</style>
