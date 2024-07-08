<template>
  <div
    :class="[
      'tag-list',
      alignment === 'left' ? 'align-left' : 'align-width',
    ]"
    :style="{ maxWidth: maxWidth }"
  >
    <div v-for="(tag, index) in tags" :key="index" class="tag">
      <span>{{ tag.text }}</span>
      <v-icon v-if="tag.icon" :size="16" :color="iconColor">
        {{ tag.icon }}
      </v-icon>
      <v-icon v-if="index < tags.length - 1" :size="16" :color="iconColor">
        mdi-circle-small
      </v-icon>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    tags: {
      type: Array,
      required: true,
    },
    alignment: {
      type: String,
      default: 'left',
    },
    maxWidth: {
      type: String,
      default: '100%',
    },
    iconColor: {
      type: String,
      default: 'primary',
    },
  },
}
</script>

<style lang="scss" scoped>
.tag-list {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}

.align-left {
  justify-content: flex-start;
}

.align-width {
  justify-content: space-between;
}

.tag {
  margin: 0 8px;
  display: flex;
  align-items: center;
}

.tag + .tag {
  margin-left: 16px;
}
</style>