<template>
    <div class="py-24 px-2 md:px-2 lg:px-24 flex flex-wrap justify-between ">
        <div @mouseenter="showToggle" @mouseleave="hideToggle" class=" h-72 w-44 md:w-36 lg:w-60 relative mb-10">
            <div v-if="hover" class="h-56 w-full absolute z-50 bgp flex flex-col py-24 px-12 hidden lg:block">
                    <button class="h-10 w-40 rounded-full bg-white hover:bg-black mb-2 text-black hover:text-white" @click="openPro">Quick View</button>
                    <button class="h-10 w-40 rounded-full bg-white hover:bg-black text-black hover:text-white" @click="cartToggle">Add to Cart</button>
                </div>
                <transition  v-if="hover" name="fade">
                <a href="#">
                        <div class="pro-5-1 h-56 w-full md:w-36 lg:w-60"></div>
                    </a>
                </transition>
                <transition  v-else name="fade">
                <a href="#">
                        <div class="pro-5 h-56 w-32 md:w-36 lg:w-60"></div>
                    </a>
                </transition>
                <div class="py-3 px-2">
                    <a href="#">Essential Pack</a> <br>
                    <span>₦7,000.00</span>
                </div>
                <div class="h-20 w-10 bg-white flex flex-col justify-between text-center rounded-full absolute bottom-20 right-2 shadow-lg-black lg:hidden">
                    <a href="#" @click="cartToggle"><i class="fal fa-shopping-cart h-10 w-10 b bg-white rounded-full icon py-3 hover:bg-black"></i></a>
                    <a href="#" @click="openPro"><i class="fal fa-eye h-10 w-10 b bg-white rounded-full py-3 icon hover:bg-black"></i></a>
            </div>
    </div>
        <div @mouseenter="showToggle2" @mouseleave="hideToggle2" class="h-72 w-40 lg:w-60 relative">
            <div v-if="hover2" class="h-56 w-full absolute z-50 bgp flex flex-col py-24 px-12 hidden lg:block">
                    <button class="h-10 w-40 rounded-full bg-white hover:bg-black mb-2 text-black hover:text-white" @click="openPro">Quick View</button>
                    <button class="h-10 w-40 rounded-full bg-white hover:bg-black text-black hover:text-white " @click="cartToggle">Add to Cart</button>
                </div>
                <transition  v-if="hover2" name="fade">
                <a href="#">
                        <div class="pro-3-1 h-56 md:w-36 lg:w-60"></div>
                    </a>
                </transition>
                <transition  v-else name="fade">
                <a href="#">
                        <div class="pro-3 h-56 md:w-36 lg:w-60"></div>
                    </a>
                </transition>
                <div class="py-3 px-2">
                    <a href="#">Sneaker Cleaner Gel</a> <br>
                    <span>₦3,500.00</span>
                </div>
                <div class="h-20 w-10 bg-white flex flex-col justify-between text-center rounded-full absolute bottom-20 right-2 shadow-lg-black lg:hidden">
                    <a href="#" @click="cartToggle"><i class="fal fa-shopping-cart h-10 w-10 b bg-white rounded-full py-3 icon hover:bg-black"></i></a>
                    <a href="#" @click="openPro"><i class="fal fa-eye h-10 w-10 b bg-white rounded-full py-3 hover:bg-black icon"></i></a>
            </div>
    </div>
        <div @mouseenter="showToggle3" @mouseleave="hideToggle3" class=" h-72  w-40 md:w-56 lg:w-60 relative">
            <div v-if="hover3" class="h-56 w-full absolute z-50 bgp flex flex-col py-24 px-12 hidden lg:block">
                    <button class="h-10 w-40 rounded-full bg-white hover:bg-black mb-2 text-black hover:text-white" @click="openPro">Quick View</button>
                    <button class="h-10 w-40 rounded-full bg-white hover:bg-black text-black hover:text-white" @click="cartToggle">Add to Cart</button>
                </div>
                <transition  v-if="hover3" name="fade">
                <a href="#">
                        <div class="pro-1-1 h-56 md:w-36 lg:w-60"></div>
                    </a>
                </transition>
                <transition  v-else name="fade">
                <a href="#">
                        <div class="pro-1 h-56 md:w-36 lg:w-60"></div>
                    </a>
                </transition>
                <div class="py-3 px-2">
                    <a href="#">Sneaker Cleaning Gel Combo</a> <br>
                    <span>₦8,000.00</span>
                </div>
                <div class="h-20 w-10 bg-white flex flex-col justify-between text-center rounded-full absolute bottom-20 right-2 shadow-lg-black lg:hidden">
                    <a href="#" @click="cartToggle"><i class="fal fa-shopping-cart h-10 w-10 b icon bg-white rounded-full py-3 hover:bg-black"></i></a>
                    <a href="#" @click="openPro"><i class="fal fa-eye h-10 w-10 b bg-white icon rounded-full py-3 hover:bg-black"></i></a>
            </div>
    </div>
        <div  @mouseenter="showToggle4" @mouseleave="hideToggle4" class=" h-72 w-40 md:w-56 lg:w-72 relative">
                <div v-if="hover4" class="h-56 w-full absolute z-50 bgp flex flex-col py-24 px-16 hidden lg:block">
                    <button class="h-10 w-40 rounded-full bg-white hover:bg-black mb-2 text-black hover:text-white" @click="openPro">Quick View</button>
                    <button class="h-10 w-40 rounded-full bg-white hover:bg-black text-black hover:text-white" @click="cartToggle">Add to Cart</button>
                </div>
                <transition  v-if="hover4" name="fade">
                <a href="#">
                        <div class="pro-4-1 h-56 md:w-36 lg:w-60"></div>
                    </a>
                </transition>
                <transition  v-else name="fade">
                <a href="#">
                        <div class="pro-4 h-56 md:w-36 lg:w-60"></div>
                    </a>
                </transition>
                <div class="py-3 px-2">
                    <a href="#">Sneaker Midsole Marker 10MM-White</a> <br>
                    <span>₦3,500.00</span>
                </div>
                <div class="h-20 w-10 bg-white flex flex-col justify-between text-center rounded-full absolute bottom-20 right-2 shadow-lg-black lg:hidden">
                    <a href="#" @click="cart"><i class="fal fa-shopping-cart h-10 w-10 b icon bg-white rounded-full py-3 hover:bg-black"></i></a>
                    <a href="#" @click="openPro"><i class="fal fa-eye h-10 w-10 b bg-white icon rounded-full py-3 hover:bg-black"></i></a>
            </div>
    </div>
        <div @mouseenter="showToggle5" @mouseleave="hideToggle5" class=" h-72 w-40 md:w-36 lg:w-60 relative">
            <div v-if="hover5" class="h-56 w-full absolute z-50 bgp flex flex-col py-24 px-12 hidden lg:block">
                    <button class="h-10 w-40 rounded-full bg-white hover:bg-black mb-2 text-black hover:text-white" @click="openPro">Quick View</button>
                    <button class="h-10 w-40 rounded-full bg-white hover:bg-black text-black hover:text-white" @click="cartToggle">Add to Cart</button>
                </div>
                <transition  v-if="hover5" name="fade">
                <a href="#">
                        <div class="pro-2-1 h-56 md:w-36 lg:w-60"></div>
                    </a>
                </transition>
                <transition  v-else name="fade">
                <a href="#">
                        <div class="pro-2 h-56 md:w-36 lg:w-60"></div>
                    </a>
                </transition>
                <div class="py-3 px-2">
                    <a href="#">Suede Cleaning Kit</a> <br>
                    <span>₦4,000.00</span>
                </div>
                <div class="h-20 w-10 bg-white flex flex-col justify-between text-center rounded-full absolute bottom-20 right-2 shadow-lg-black lg:hidden">
                    <a href="#" @click="cartToggle"><i class="fal fa-shopping-cart h-10 w-10 b bg-white icon rounded-full py-3 hover:bg-black"></i></a>
                    <a href="#" @click="openPro"><i class="fal fa-eye h-10 w-10 b bg-white rounded-full icon py-3 hover:bg-black"></i></a>
            </div>
    </div>
    <transition name="slide-fade">
                <div v-if="cart" class="fixed top-0 right-0 w-80 z-50 bg-white h-screen">
                    <div class="flex justify-between px-5 h-16 border">
                        <h1 class="my-5 text-l">SHOPPING CART</h1>
                        <button @click="cartToggle" class="text-2xl">X</button>
                    </div>
                    <div class="px-4 py-7 h-96 border border-y-2 border-b-0">
                        <div class="flex  text-start mb-8">
                            <div class="bg-shop h-32 w-32" alt=""></div>
                            <div class="ml-3">
                                <h1>Essential Pack</h1>
                                <p class="text-gray-400">₦7,000.00</p>
                                <i class="fas fa-bin"></i>
                            </div>
                        </div>

                    </div>
            </div>
        </transition> 
        <transition name="fade">
            <div @click="cartToggle" v-if="cart" class="h-screen w-full fixed top-0 left-0 z-20 bg "></div>
        </transition>
</div>
</template>

<script>
export default {
    name: '',
    data() {
        return {
            hover: false,
            hover2: false,
            hover3: false,
            hover4: false,
            hover5: false,
            cart: false
        }
    },
    methods: {
        showToggle() {
            this.hover = true
        },
        hideToggle() {
            this.hover =false
        },
        showToggle2() {
            this.hover2 = true
        },
        hideToggle2() {
            this.hover2 =false
        },
        showToggle3() {
            this.hover3 = true
        },
        hideToggle3() {
            this.hover3 =false
        },
        showToggle4() {
            this.hover4 = true
        },
        hideToggle4() {
            this.hover4 =false
        },
        showToggle5() {
            this.hover5 = true
        },
        hideToggle5() {
            this.hover5 =false
        },
        openPro() {
            this.$emit('open')
        },
        cartToggle() {
                this.cart = !this.cart
            }
    }
    }
</script>

<style scoped>
    span{
        color:#696969;
    }
    .icon:hover{
        color: white;
    }
    .bgp{
        background-color: #87878765;
    }
    .pro-1{
        background-image: url(https://cdn.shopify.com/s/files/1/0263/2430/3946/products/2_5f499a4a-25b0-4139-bddd-8a5a28a70f7f_540x.png?v=1625041768);
        background-position: center;
        background-size: 15rem;
    }
    .pro-1-1{
        background-image: url("https://cdn.shopify.com/s/files/1/0263/2430/3946/products/1_2c2141db-f4b4-43e7-bfd6-235cc77cfbcc_1296x.png?v=1625041768");
        background-position: center;
        background-size: 15rem;
    }
    .pro-2{
        background-image: url(https://cdn.shopify.com/s/files/1/0263/2430/3946/products/SuedeCleaningKit_533eb8d3-8dfe-4355-9b1d-8e4975562657_360x.png?v=1616150388);
        background-position: center;
        background-size: 18rem;
    }
    .pro-2-1{
        background-image: url("https://cdn.shopify.com/s/files/1/0263/2430/3946/products/2_058a5f2c-19e1-4259-9be3-bf1c6de944f0_1296x.png");
        background-position: center;
        background-size: 18rem;
    }
    .pro-3{
        background-image: url(https://cdn.shopify.com/s/files/1/0263/2430/3946/products/1_e9420ae9-54e1-4230-a87b-ee753d0ee80b_360x.png?v=1625041851);
        background-position: center;
        background-size: 16rem;
    }
    .pro-3-1{
        background-image: url("https://cdn.shopify.com/s/files/1/0263/2430/3946/products/Single_1296x.png?v=1625041851");
        background-position: center;
        background-size: 16rem;
    }
    .pro-5{
        background-image: url(https://cdn.shopify.com/s/files/1/0263/2430/3946/products/Untitleddesign_69338fff-a36a-4d07-ae57-3609143c5f02_180x.png?v=1660228614);
        background-position: center;
        background-size: 14rem;
    }
    .pro-5-1{
        background-image: url("https://cdn.shopify.com/s/files/1/0263/2430/3946/products/untitled162_1296x.jpg?v=1660230175");
        background-position: center;
        background-size: 15rem;
    }
    .pro-4{
        background-image: url(https://cdn.shopify.com/s/files/1/0263/2430/3946/products/pixlr-bg-result_2_360x.png?v=1638529305);
        background-position: center;
        background-size: 14rem;
        transition: 1s;
    }
    .pro-4-1{
        background-image: url("https://cdn.shopify.com/s/files/1/0263/2430/3946/products/IMG_9889_1296x.jpg?v=1638529390");
        background-position: center;
        background-size: 16rem;
        transition: 1s;
    }

    .bg{
        background-color: rgba(0, 0, 0, 0.6);
    }

    .bg-shop{
        background-image: url(https://cdn.shopify.com/s/files/1/0263/2430/3946/products/Untitleddesign_69338fff-a36a-4d07-ae57-3609143c5f02_180x.png?v=1660228614);
        background-size: 10rem;
        background-position: center;

    }
    .slide-fade-enter-active {
        transition: all 0.2s ease-in;
        position: absolute;
        right: 0;
        }

      .slide-fade-leave-active {
        transition: all 0.2s;
        position: absolute;
        right: -800px;
        }

       .slide-fade-enter-from,
       .slide-fade-leave-to {
        opacity: 0;
        position: absolute;
        right: -800px;
        }
        .fade-enter-from,
        .fade-leave-to {
        opacity: 0;
        }
    @media (max-width: 770px) {
        .pro-1,.pro-2,.pro-3{
            background-size: 12rem;
        }
        .pro-4{
            background-size: 13rem;
        }
        .fade-enter-active,
        .fade-leave-active {
        transition: opacity 0.5s ease;
        }

        .fade-enter-from,
        .fade-leave-to {
        opacity: 0;
        }
    }
    @media (max-width: 380px) {
        .pro-1,.pro-2,.pro-3{
            background-size: 10rem;
            background-repeat: no-repeat;
        }
        .pro-4, .pro-5{
            background-size: 10rem;
            background-repeat: no-repeat;
        }
    }
</style>