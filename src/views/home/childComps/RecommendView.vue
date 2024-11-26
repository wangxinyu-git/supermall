<template>
  <div class="recommend">
    <div
      class="recommend-item"
      v-for="(item, index) in recommends"
      :key="index"
    >
      <a :href="item.link">
        <img :src="item.image" alt="" />
        <span>{{ item.title }}</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    recommends: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.recommend {
  display: flex;
  margin-top: 10px;
  font-size: 12px;
  padding-bottom: 10px;
  border-bottom: 10px solid #eee;
}

.recommend-item {
  flex: 1;
  text-align: center;
}

.recommend img {
  width: 70px;
  height: 70px;
  margin-bottom: 10px;
}
</style>