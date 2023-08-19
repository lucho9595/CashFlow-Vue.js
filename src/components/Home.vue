<template>
  <div>
    <Layout>
      <template #header>
        <Header></Header>
      </template>
      <template #resume>
        <Resume :label="label" :total-amount="100000" :amount="amount" :totalLabel="'Ahorro Total'">
          <template #graphic>
            graphic
          </template>
          <template #action>
            action
          </template>
        </Resume>
      </template>
      <template #movements>
        <Movements />
      </template>
    </Layout>
  </div>
</template>

<script>
import Layout from './Layout.vue';
import Header from './Header.vue';
import Resume from './Resume/Index.vue';
import Movements from './Movements/Index.vue';

export default {
  components: {
    Layout,
    Header,
    Resume,
    Movements
  },
  data() {
    return {
      amount: null,
      label: '18 de Agosto del 2023'
    }
  },
};
</script>