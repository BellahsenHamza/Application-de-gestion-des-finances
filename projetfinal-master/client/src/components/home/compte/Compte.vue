<template>
  <div class="container" id="compte">
    <div class="card">
      <div class="card-header">
        <div class="card-header-title">{{compte.NomCompte}} - {{typeCompte}}</div>
      </div>
      <div class="card-footer">
        <a href="" class="card-footer-item" v-on:click.prevent="seeInvestissements()">
          Planifiez vos investissements
        </a>
        <a href="" class="card-footer-item" v-on:click.prevent="updateCompte">
          Modifier le compte
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import CompteEdit from './CompteEdit.vue';

export default {
  name: 'Compte',
  props: {
    compte: Object,
  },
  computed: {
    typeCompte() {
      if (this.compte.IdTypeCompte === 1) return 'CELI';
      if (this.compte.IdTypeCompte === 2) return 'REER';
      if (this.compte.IdTypeCompte === 3) return 'NE';
      if (this.compte.IdTypeCompte === 4) return 'REEE';
      return 'Type Compte';
    },
  },
  methods: {
    updateCompte() {
      this.$buefy.modal.open({
        parent: this,
        component: CompteEdit,
        props: this.compte,
        hasModalCard: true,
        customClass: 'custom-class custom-class-2',
        trapFocus: true,
      });
    },
    seeInvestissements() {
      this.$store.dispatch('compte/setCurrCompteId', this.compte.IdCompte);
      this.$router.push({ name: 'Investissement' });
    },
  },
};
</script>

<style scoped lang="scss">
.card-header{
  margin-bottom: 0;
}
</style>
