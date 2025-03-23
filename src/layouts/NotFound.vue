<template>
  <q-layout view="lhr LpR lfr" class="flex justify-center items-center">
    <div style="width: 80dvw; height: 80dvh;">
      <div class="col-md-4 q-pa-md text-center">
        <img src="../assets/not_found.svg" width="600dvw">
      </div>
      <div class="col-md-4 q-pt-lg text-center text-h5">Oops! Looks like you're lost. Try getting back on track or explore somewhere else!</div>
      <div class="col-md-4 text-center text-small text-bold text-grey">404 Not Found</div>
      <div class="col-md-4 q-pt-lg text-center text-small text-bold text-grey">
        <q-btn color="primary" label="Explore" icon="rocket_launch" to="/"/>
      </div>
    </div>

  </q-layout>
</template>

<script>
export default {
  data() {
    return {
    }
  },
  methods: {
  },
}
</script>
