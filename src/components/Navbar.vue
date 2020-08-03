<template>
    
    <nav class="navbar navbar-expand-sm navbar-light bg-dark text-light" data-toggle="affix">
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
                
                
                <router-link class="nav-link text-light" to="/" tag="li" data-toggle="collapse" data-target="#navbars4"><a>Home</a></router-link>
                <router-link class="nav-link text-light" to="/about" tag="li" data-toggle="collapse" data-target="#navbars4"><a>About</a></router-link>
                    
                <li class="nav-item">
                    <div class="triple-deco-container container">
                        <div class="triple-deco-content ">JAN-MADE</div>
                        <div class="triple-deco-tall"></div>
                        <div class="triple-deco-mid"></div>
                        <div class="triple-deco-wide"></div>
                    </div>
                    <!-- <a class="navbar-brand d-none d-sm-block" href="#">JAN-MADE</a> -->
                </li> 
                <a class="nav-link text-light" href="http://jetk.github.io" tag="li">Blog</a>
                <router-link class="nav-link text-light" to="/contact" tag="li" data-toggle="collapse" data-target="#navbars4"><a style="white-space: nowrap;">Contact & CV</a></router-link>
                
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


<style scoped>

a:hover a text-light:hover{
    
    text-shadow: 0px 0px 3px hotpink;
    text-decoration: none;
}

li a {
    color: white;
}

.navbar-toggler {
    border: none;
    width: 100%;
}

.nav-link{
    width: 10vw;
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
  color: white
/*   background-color: lightblue; */
/*   color: #000; */
}

.triple-deco-container .triple-deco-tall {
  grid-area: tall;
  border: 1.5px solid gold;
}

.triple-deco-container .triple-deco-mid {
  grid-area: mid;
  border: 2px solid goldenrod;
}

.triple-deco-container .triple-deco-wide {
  grid-area: wide;
  border: 1.5px solid gold;

}

@media (max-width: 576px) {
    .navbar-collapse .triple-deco-container {
        display: none !important;
    }
}

</style>