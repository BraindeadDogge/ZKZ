<template>
  <v-card color="basil">
    <v-card-title class="text-center justify-center py-6">
      <h1 class="font-weight-bold display-1 basil--text" style="white-space: nowrap">КОМПЛЕКСНАЯ ПЕРЕРАБОТКА КУКУРУЗЫ</h1>
    </v-card-title>

    <v-tabs
      v-model="tab"
      background-color="transparent"
      color="basil"
      grow
      height="1.5px"
    >
      <v-tab
        v-for="item in items"
        :key="item"
      >
        {{ item }}
      </v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item>
        <v-card
          color="basil"
          flat
        >
          <v-card-text><div><strong>При комплексной переработке кукурузы кроме крахмала и крахмалопродуктов получают ряд ценных побочных продуктов, таких как:</strong><br><br> - <strong>Глютен</strong> &ndash;  является ценной белковой добавкой в  кормах для животных  благодаря содержанию основных аминокислот и сбалансированных белков  кукурузы. Глютен применяется в составе комбикормов в сочетании с другими ингридиентами.<br><br>   - <strong>Кукурузный зародыш </strong>&ndash; основное сырье для производства кукурузного масла, которое благодаря содержанию ненасыщенных жирных кислот является ценным пищевым продуктом.<br><br> - <strong>Экстракт кукурузы </strong>&ndash; концентрат растворимых веществ, полученный в результате процесса замачивания кукурузы. Экстракт содержит не менее 40% белка и используется как добавка к корму крупного рогатого скота. Так же экстракт используется производителями антибиотиков в качестве питательной среды.<br><br> - <strong>Корм из кукурузного жмыха </strong>&ndash; для  животных сельскохозяйственного назначения.<br> <br><br></div></v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>

<script>
  export default {
    data () {
      return {
        tab: null,
        items: [
          ''
        ]
      }
    },
  }
</script>

<style>
/* Helper classes */
.basil {
  background-color: #FFFBE6 !important;
}
.basil--text {
  color: #356859 !important;
}
</style>