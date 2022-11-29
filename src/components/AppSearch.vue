<template>
  <div>
    <label for="value">
      <select
        v-model="value"
        @change="$emit('change', value)"
      >
        <option value="none" />
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
      </select>
    </label>
    <button
      class="btn btn-primary mx-1"
      @click="$emit('change', value)"
    >
      Search
    </button>
  </div>
</template>

<script>
export default {
  name: 'AppSearch',
  data() {
    return {
      value: 'none',
    };
  },
};
</script>

<style lang="scss" scoped>
</style>
