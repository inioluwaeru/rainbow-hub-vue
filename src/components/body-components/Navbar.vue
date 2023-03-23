<template>
    <div class="h-28 bg-white flex justify-between text-center">
            <div class="lg:hidden my-10 mx-5">
                <i @click="navToggle" class="fas fa-indent"></i>
            </div>
            <transition name="slide-fade">
                <div v-if="nav" class=" fixed top-0 left-0 w-80 z-50 bg-white h-screen">
                <div class="flex justify-between">
                    <button class=" border-b-2 border-gray-600 bg-gray-200 w-40 h-16">Menu</button>
                    <button class="  border-gray-600 w-40 h-16">Categories</button>
                </div>
                <div class="flex flex-col text-start text-black">
                <a href="#" class="text-xl h-16 py-6 px-4 w-full border font-semilight leading-6 text-gray-600">Shop</a>
                <a href="#" class="text-xl h-16 py-6 px-4 w-full border font-semilight leading-6 text-gray-600">Sneaker Care</a>
                <a href="#" class="text-xl h-16 py-6 px-4 w-full border font-semilight leading-6 text-gray-600">FAQs</a>
                <a href="#" class="text-xl h-16 py-6 px-4 w-full border font-semilight leading-6 text-gray-600">Blog</a>
                <a href="#" class="text-xl h-16 py-6 px-4 w-full border font-semilight leading-6 text-gray-600">Search</a>
                <a href="#" class="text-xl h-16 py-6 px-4 w-full border font-semilight leading-6 text-gray-600">Login / Register</a>
            </div>
            <div class="text-start h-40 py-6 px-4 border">
                <h1 class="mb-5">Need help?</h1>
                <p class="mb-4 text-gray-400"><i class="far fa-phone text-gray-400"></i> &nbsp; +234 913 503 7348</p>
                <p class="text-gray-400"><i class="far fa-envelope text-gray-400"></i> &nbsp; info@shwype.com</p>
            </div>
            </div>
        </transition> 
        <transition name="fade">
            <div @click.self="navToggle" v-if="nav"  class="h-screen w-full fixed top-0 left-0 z-20 bg ">
                <button @click.self="navToggle" class="h-16 md:h-20 w-12 md:w-20 bg-black text-white ml-80 md:mr-12 text-3xl">X</button>
            </div>
        </transition>
            <div class="py-10 hidden lg:flex">
                <a href="#" class="ml-5">Shop</a>
                <a href="#" class="ml-5">Sneaker Care</a>
                <a href="#" class="ml-5">FAQS</a>
                <a href="#" class="ml-5">Blog</a>
            </div>  
           
            <img src="../../assets/img/logo.avif" class="ml-12 md:ml-48 lg:ml-0" width="100px" alt="">
            <div class="nav-btns flex py-10">
                <a class="mr-5" href="#" @click="cartToggle"><button class="h-8 w-8 icon-cart"></button></a>
                <a class="mr-5 hidden md:block" href="#" @click="accountToggle"><button class="h-8 w-8 icon-profile"></button></a>
                <a class="mr-5" href="#" @click="searchToggle"><button class="h-8 w-8 icon-lens"></button></a>
            </div>
            <transition name="slide-r-fade">
                <div v-if="search" class="fixed top-0 right-0 w-80 z-50 bg-white h-screen">
                    <div class="flex justify-between px-5 h-16 border">
                        <h1 class="my-5 text-l">SEARCH OUR SITE</h1>
                        <button @click="searchToggle" class="text-2xl">X</button>
                    </div>
                    <div class="flex justify-between px-5 py-7 h-28 border border-y-2">
                        <input type="text" placeholder="Search for products" class="h-12 w-72 border border-gray-500 rounded-full px-3">
                    </div>
                
            </div>
        </transition> 
        <transition name="fade">
            <div @click="searchToggle" v-if="search" class="h-screen w-full fixed top-0 left-0 z-20 bg "></div>
        </transition>

        <!------------- Account Login------- -->
            <transition name="slide-r-fade">
                <div v-if="account" class="fixed top-0 right-0 w-80 z-50 bg-white h-screen">
                    <div class="flex justify-between px-5 h-16 border">
                        <h1 class="my-5 text-l">LOGIN</h1>
                        <button @click="accountToggle" class="text-2xl">X</button>
                    </div>
                    <div class="px-4 py-7 h-96 border border-y-2 border-b-0">
                        <div class="flex flex-col text-start mb-8">
                            <p class="mb-4">Email <span>*</span></p>
                            <input type="text" class="h-12 w-72 border border-gray-500">
                        </div>
                        <div class="flex flex-col text-start mb-5">
                            <p class="mb-4">Password <span>*</span></p>
                            <input type="text" class="h-12 w-72 border border-gray-500">
                        </div>
                        <button class="h-12 w-72 border border-gray-500 rounded-full bg-black text-white text-xl font-bold">SIGN IN</button>
                            <div class="flex gap-2 mt-3">
                                <p class="text-gray-400">New customer?</p>
                                <a href="#">Create your account</a>
                            </div>
                            <div class="flex gap-2 mt-3">
                                <p class="text-gray-400">Lost password?</p>
                                <a href="#">Recover password</a>
                            </div>
                    </div>
                    
                
            </div>
        </transition> 
        <transition name="fade">
            <div @click="accountToggle" v-if="account" class="h-screen w-full fixed top-0 left-0 z-20 bg "></div>
        </transition>

<!-- ------------------------Cart---------------- -->

            <transition name="slide-r-fade">
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
            nav: false,
            search: false,
            account: false,
            cart: false
        }
    },
    methods: {
        navToggle() {
                this.nav = !this.nav
            },
        searchToggle() {
                this.search = !this.search
            },
        accountToggle() {
                this.account = !this.account
            },
        cartToggle() {
                this.cart = !this.cart
            }
        }
    }
</script>
<style scoped>
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
        left: 0;
        }

      .slide-fade-leave-active {
        transition: all 0.2s;
        position: absolute;
        left: -800px;
        }

       .slide-fade-enter-from,
       .slide-fade-leave-to {
        opacity: 0;
        position: absolute;
        left: -800px;
        }
    .slide-r-fade-enter-active {
        transition: all 0.2s ease-in;
        position: absolute;
        right: 0;
        top: 0;
        }

      .slide-r-fade-leave-active {
        transition: all 0.2s;
        position: absolute;
        right: -800px;
        top: 0;
        }

       .slide-r-fade-enter-from,
       .slide-r-fade-leave-to {
        opacity: 0;
        position: absolute;
        right: -800px;
        top:0;
        }
        .fade-enter-active,
        .fade-leave-active {
        transition: opacity 0.5s ease;
        }

        .fade-enter-from,
        .fade-leave-to {
        opacity: 0;
        }
        .icon-cart{
            background-image: url(../../assets/img/cart-outline.svg);
            background-size: 31px;
        }
        .icon-profile{
            background-image: url(../../assets/img/account.svg);
            background-size: 31px;
        }
        .icon-lens{
            background-image: url(../../assets/img/magnify.svg);
            background-size: 31px;
        }
        span{
        color: red;
        }
</style>