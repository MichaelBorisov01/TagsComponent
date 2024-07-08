<template>
  <div class="app">
    <!-- Компонент на всю ширину экрана с выравниванием по левому краю -->
    <v-card class="app__card">
      <v-card-title class="app__card-title">Компонент на всю ширину экрана с выравниванием по левому краю</v-card-title>
      <v-card-text class="app__card-text">
        <TagList
          :tags="tags"
          alignment="left"
          :max-width="'100%'"
        />
      </v-card-text>
    </v-card>

    <!-- Компонент на всю ширину экрана с выравниванием по ширине -->
    <v-card class="app__card">
      <v-card-title class="app__card-title">Компонент на всю ширину экрана с выравниванием по ширине</v-card-title>
      <v-card-text class="app__card-text">
        <TagList
          :tags="tags"
          alignment="width"
          :max-width="'100%'"
        />
      </v-card-text>
    </v-card>

    <!-- Компонент на 50% ширины экрана с выравниванием по левому краю и по ширине -->
    <div class="app__flex-container">
      <v-card class="app__card app__card_half">
        <v-card-title class="app__card-title">Компонент на 50% ширины экрана с выравниванием по левому краю</v-card-title>
        <v-card-text class="app__card-text">
          <TagList
            :tags="tags"
            alignment="left"
            :max-width="'100%'"
          />
        </v-card-text>
      </v-card>
      <v-card class="app__card app__card_half">
        <v-card-title class="app__card-title">Компонент на 50% ширины экрана с выравниванием по ширине</v-card-title>
        <v-card-text class="app__card-text">
          <TagList
            :tags="tags"
            alignment="width"
            :max-width="'100%'"
          />
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
import TagList from './components/TagList.vue'

export default {
  components: { TagList },
  data() {
    return {
      tags: [
        { text: 'текст1' },
        { text: 'текст2', icon: 'mdi-arm-flex' },
        { text: 'текст3' },
        { text: 'текст4', icon: 'mdi-alien-outline' },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.app {
  &__card {
    margin-bottom: 16px;
  }

  &__card-title {
    font-size: 18px;
    font-weight: bold;
  }

  &__card-text {
    padding: 16px;
  }

  &__flex-container {
    display: flex;
    justify-content: space-between;
  }

  &__card_half {
    width: 50%;
    margin-right: 16px;

    &:last-child {
      margin-right: 0;
    }
  }
}</style>