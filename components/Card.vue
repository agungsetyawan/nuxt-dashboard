<template>
  <div class="card card-img-holder text-white" :class="bgVariant">
    <div class="card-body">
      <img
        src="~assets/images/circle.svg"
        alt="circle-image"
        class="card-img-absolute"
      />
      <slot />
      <!-- <h4 class="font-weight-normal mb-3">
        Weekly Sales
        <i class="mdi mdi-chart-line mdi-24px float-right"></i></h4>
      <h2 class="mb-5">$ 15,0000</h2>
      <h6 class="card-text">Increased by 60%</h6> -->
    </div>
  </div>
</template>

<script>
export default {
  props: {
    bgVariant: {
      type: String,
      default: 'bg-gradient-primary'
    }
  }
}
</script>
