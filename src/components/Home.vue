<template>
  <Layout>
    <template #header>
      <Header></Header>
    </template>
    <template #resume>
      <Resume
        :total-label="'Ahorro total'"
        :label="label"
        :total-amount="100000"
        :amount="amount"
      >
        <template #graphic> Graphic </template>
        <template #action> action </template>
      </Resume>
    </template>
    <template #movements>
      <Movements :movements="movements" />
    </template>
  </Layout>
</template>

<script>
import Layout from "./Layout.vue";
import Header from "./Header.vue";
import Resume from "./Resume/Index.vue";
import Movements from "./Movements/Index.vue";

export default {
  components: {
    Layout,
    Header,
    Resume,
    Movements,
  },
  data() {
    return {
      label: null,
      amount: null,
      movements: [
        {
          id: 0,
          title: "Movimiento 1",
          description: "Lorem ipsum dolor sit amet",
          amount: 1000,
        },
        {
          id: 1,
          title: "Movimiento 2",
          description: "Lorem ipsum dolor sit amet",
          amount: 1000,
        },
        {
          id: 2,
          title: "Movimiento 3",
          description: "Lorem ipsum dolor sit amet",
          amount: -11000,
        },
        {
          id: 3,
          title: "Movimiento 4",
          description: "Lorem ipsum dolor sit amet",
          amount: -1000,
        },
        {
          id: 4,
          title: "Movimiento 5",
          description: "Lorem ipsum dolor sit amet",
          amount: -5000,
        },
        {
          id: 5,
          title: "Movimiento 6",
          description: "Lorem ipsum dolor sit amet",
          amount: 1000,
        },
        {
          id: 6,
          title: "Movimiento 7",
          description: "Lorem ipsum dolor sit amet",
          amount: 1000,
        },
        {
          id: 7,
          title: "Movimiento 8",
          description: "Lorem ipsum dolor sit amet",
          amount: 1000,
        },
      ],
    };
  },
};
</script>

<style scoped>
.movements {
  max-height: 100%;
  padding: 0 8px;
  margin-bottom: 14px;
}

.title {
  margin: 8px 16px 24px 16px;
  color: var(--brand-blue);
}

.content {
  max-height: 68vh;
  display: flex;
  flex-direction: column;
  gap: 8px;
  overflow-y: scroll;
}
</style>
