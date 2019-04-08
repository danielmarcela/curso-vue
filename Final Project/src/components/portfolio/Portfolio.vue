<template>
    <div>
        <button @click="con">dasd</button>
        <app-stock v-for="stock in stocks" :stock="stock"></app-stock>
    </div>
</template>

<script>
    import {mapGetters} from 'vuex';
    import Stock from './Stock.vue';

    export default{
        computed: {
            ...mapGetters([{
                stocks: 'stockPortfolio'
            }])
        },
        components: {
            appStock: Stock
        },
        methods: {
            con() {
                console.log(this.stock);
                for (let i = 0; i < this.stocks.length; i++){
                    console.log(this.stocks);
                }
            }
        }
    }
</script>