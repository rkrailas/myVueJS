<template>
  <div>
    <Clock>
      <span style="color:red;">เวลาปัจจุบัน</span>
    </Clock>
    <Clock>
      <span style="color:green;">เวลาปัจจุบัน</span>
    </Clock>

    <!-- Using fallback (default) content -->
    <clock />

    <br><br>
    <Clock>
      <template v-slot:header>
        <div>Header content</div>        
      </template>

      <template v-slot:footer>
        <div>Footer content</div>        
      </template>
    </Clock>
  </div>
</template>

<script>
import Clock from "@/components/helpers/Clock.vue";
export default {
  name: "Demo7",
  components: {
    Clock,
  },
};
</script>

<style></style>
