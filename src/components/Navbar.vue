<template>
    
    <nav class="navbar navbar-expand-sm navbar-light" data-toggle="affix">
    <div class="container flex-sm-nowrap align-items-baseline justify-content-center ">
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbars4" aria-expanded="false" aria-label="Toggle navigation">
           <div class="triple-deco-container container">
                        <div class="triple-deco-content">JAN-MADE</div>
                        <div class="triple-deco-tall"></div>
                        <div class="triple-deco-mid"></div>
                        <div class="triple-deco-wide"></div>
            </div>
        </button>
           
        <div class="collapse navbar-collapse text-center" id="navbars4">
            <ul class="navbar-nav nav-fill w-100">
                <li class="nav-item">
                    <router-link class="nav-link" to="/">Home</router-link>
                </li>
                <li class="nav-item">
                    <router-link class="nav-link" to="/about">About</router-link>
                </li>
                <li>
                    <div class="triple-deco-container container">
                        <div class="triple-deco-content ">JAN-MADE</div>
                        <div class="triple-deco-tall"></div>
                        <div class="triple-deco-mid"></div>
                        <div class="triple-deco-wide"></div>
                    </div>
                    <!-- <a class="navbar-brand d-none d-sm-block" href="#">JAN-MADE</a> -->
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="https://jetk.github.io">Blog</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Link</a>
                </li>
            </ul>
        </div>
    </div>
</nav>
</template>

<script>
    export default {
        data() {
            return {
                mobileNavCollapsed: false
            }
        },
        methods: {
            collapse() {
                this.mobileNavCollapsed = !this.mobileNavCollapsed
            }
        },
    }
</script>


<style .scoped>

.navbar-toggler {
    border: none;
    width: 100%
}

    /******** TRIPLE *********/
.triple-deco-container {
  display: grid !important;
  align-items: stretch !important;
  grid-template-columns: 
    [wide-start]  5px 
    [mid-start]   5px 
    [tall-start]  1fr 
    [tall-end]    5px 
    [mid-end]     5px 
    [wide-end] 
  ;
  grid-template-rows: 
    [tall-start]  5px 
    [mid-start]   5px 
    [wide-start]  1fr 
    [wide-end]    5px 
    [mid-end]     5px 
    [tall-end] 
  ;
/*   background-color: peachpuff; */
}

.triple-deco-container .triple-deco-content {
  grid-column: tall-start / tall-end;
  grid-row: wide-start / wide-end;
  padding: 5px 10px;
/*   background-color: lightblue; */
/*   color: #000; */
}

.triple-deco-container .triple-deco-tall {
  grid-area: tall;
  border: 1px solid gold;
}

.triple-deco-container .triple-deco-mid {
  grid-area: mid;
  border: 1px solid goldenrod;
}

.triple-deco-container .triple-deco-wide {
  grid-area: wide;
  border: 1px solid gold;

}

@media (max-width: 576px) {
    .navbar-collapse .triple-deco-container {
        display: none !important;
    }
}

</style>