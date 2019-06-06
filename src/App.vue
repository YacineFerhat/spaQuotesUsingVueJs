<template>
  <div class="container">
    <app-new-quotes @quoteAdded="newQuote"></app-new-quotes>
    <app-Quote-Grid :quotes="quotes"></app-Quote-Grid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">
          Info: Click on a quote to delete it!
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import QuoteGrid from './components/QuoteGrid';
  import NewQuotes from './components/NewQuotes';

  export default {
    data : function(){
      return{
        quotes : [
          'Just a quote'
        ],
        maxQuotes : 10
      }
    },
    components:{
      appQuoteGrid : QuoteGrid,
      appNewQuotes : NewQuotes
    },
    methods : {
      newQuote(quote){
        this.quotes.push(quote);
      }
    }
  }
</script>


<style>

</style>
