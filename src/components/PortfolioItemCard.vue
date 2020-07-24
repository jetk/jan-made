<template>
    <div class="col-auto mb-4">
        <div class="card" style="width:18rem; height:24rem">
            <div class="trapezoid trapezoid-outer"></div>
            <div class="trapezoid">
                <span style="font-size: 1.20rem; font-weight:bold; color:black;">{{cardData.displayName | capitalize }}</span>
            </div>
            <img class="card-img-top" style="height: 18rem"
                :src="require(`@/assets/${cardData.img}.png`)"
                alt="Card image cap">
            <!-- <img class="card-img-top" style="height: 18rem"
                src="https://images-na.ssl-images-amazon.com/images/I/51DvCss8J3L._AC_SY679_.jpg"
                alt="Card image cap"> -->
            <div class="card-body">
                <p class="card-text">{{cardData.blurb}}</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['info', 'cardData'],
        filters: {
            capitalize: function (value) {
                if (!value) return ''
                return value.toString().toUpperCase()
            }
        }
    }
</script>


<style>
    .card {
        border: 2px solid goldenrod;
        border-radius: 5px;
    }

    .trapezoid {
        width: 250px;
        height: 40px;
        background:whitesmoke;
        border: 2px solid goldenrod;
        transform: perspective(10px) rotateX(-2deg);
        position: absolute;
        margin-left: auto;
        margin-right: auto;
        left: 0;
        right: 0;
        text-align: center;
    }

    .trapezoid-outer {
        width: 260px;
        height: 45px;
    }
</style>