<template>
  <div>
    <!-- Компонент на всю ширину экрана с выравниванием по левому краю -->
    <v-card style="margin-bottom: 16px;">
      <v-card-title>Компонент на всю ширину экрана с выравниванием по левому краю</v-card-title>
      <v-card-text>
        <TagList
          :tags="tags"
          alignment="left"
          :max-width="'100%'"
        />
      </v-card-text>
    </v-card>

    <!-- Компонент на всю ширину экрана с выравниванием по ширине -->
    <v-card style="margin-bottom: 16px;">
      <v-card-title>Компонент на всю ширину экрана с выравниванием по ширине</v-card-title>
      <v-card-text>
        <TagList
          :tags="tags"
          alignment="width"
          :max-width="'100%'"
        />
      </v-card-text>
    </v-card>

    <!-- Компонент на 50% ширины экрана с выравниванием по левому краю -->
    <v-card style="width: 50%; display: inline-block; margin-bottom: 16px;">
      <v-card-title>Компонент на 50% ширины экрана с выравниванием по левому краю</v-card-title>
      <v-card-text>
        <TagList
          :tags="tags"
          alignment="left"
          :max-width="'100%'"
        />
      </v-card-text>
    </v-card>

    <!-- Компонент на 50% ширины экрана с выравниванием по ширине -->
    <v-card style="width: 50%; display: inline-block; margin-left: 16px; margin-bottom: 16px;">
      <v-card-title>Компонент на 50% ширины экрана с выравниванием по ширине</v-card-title>
      <v-card-text>
        <TagList
          :tags="tags"
          alignment="width"
          :max-width="'100%'"
        />
      </v-card-text>
    </v-card>
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
        { text: 'текст2', icon: 'mdi-star' },
        { text: 'текст3' },
        { text: 'текст4', icon: 'mdi-heart' },
      ],
    }
  },
}
</script>