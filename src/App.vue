<template>
  <div :class="$style.container">
    <Form
      v-model:name="form.name"
      v-model:surname="form.surname"
      @submit="onSubmit"
    />
  </div>
</template>

<script>
import { ref } from 'vue';
import Form from './components/Form.vue';

export default {
  components: {
    Form,
  },
  setup() {
    const form = ref({
      name: '',
      surname: '',
    });

    const onSubmit = () => console.log(form);

    return {
      form,
      onSubmit,
    };
  },
};
</script>

<style module>
.container {
  max-width: 30rem;
  @apply mx-auto py-8;
}
</style>
