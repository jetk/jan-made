<template>
    <div class="card" style="position: relative;">
        <div class="trapezoid trapezoid-outer"></div>
        <div class="trapezoid"> <h2>PROJECT {{info}}</h2> </div>
    <!-- <div class="card-header">
    <h5 style="margin-bottom: 0">ISSRAN</h5>
  </div> -->
  <img class="card-img-top" style="height: 300px" src="https://images.unsplash.com/photo-1594643566940-893b456ae452?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80" alt="Card image cap">
  <div class="card-body">
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
  </div>
</div>
</template>

<script>
export default {
    props: ['info'],
}
</script>


<style>
    .card {
        border: 3px solid goldenrod;
        border-radius: 5px;
    }

    .trapezoid {
        width: 200px;
        height: 50px;
        background: white;
        border: 2px solid goldenrod;
        color: black;
        transform: perspective(10px) rotateX(-2deg);
        position: absolute;
        margin-left: auto;
        margin-right: auto;
        left: 0;
        right: 0;
        text-align: center;
    }

    .trapezoid-outer {
        width: 210px;
        height: 55px;
    }
</style>
