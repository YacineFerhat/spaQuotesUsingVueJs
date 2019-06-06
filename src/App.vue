<template>
  <div class="container">
    <app-Header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-Header>
    <app-new-quotes @quoteAdded="newQuote"></app-new-quotes>
    <app-Quote-Grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-Quote-Grid>
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
  import Header from './components/header.vue';
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
      appHeader : Header,
      appQuoteGrid : QuoteGrid,
      appNewQuotes : NewQuotes
    },
    methods : {
      newQuote(quote){
        if(this.quotes.length>= this.maxQuotes){
          return alert('Hey, please delete a quote first =)')
        }
        this.quotes.push(quote);
      },
      deleteQuote(index){
        this.quotes.splice(index,1);
      }
    }
  }
</script>


<style>

</style>
