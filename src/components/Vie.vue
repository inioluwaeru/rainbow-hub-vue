<template>
  <div class="bg fixed w-full h-screen z-50 py-0 md:py-60 lg:py-5 px-2.5 md:px-1 lg:px-36" @click.self="close">
    <div class="w flex flex-col md:flex-row overflow-scroll">
      <div class="w-full md:w-3/5 f relative">
        <transition-group name='fade' tag='div'>
          <div v-for="i in [currentIndex]" :key='i' >
            <img class="h-full" :src="currentImg"/>
          </div>
        </transition-group> 
        <div class="absolute top-40 md:top-56 lg:top-72 flex justify-between w-full px-5">
          <button class="prev text-black text-2xl px-4 py-1.5 h-12 w-12 border border-black rounded-full" @click="prev" href='#'>&#10094;</button>
          <button class="next text-black text-2xl px-4 py-1.5 h-12 w-12 border border-black rounded-full" @click="next" href='#'>&#10095;</button>
        </div>
        <button class="h-12 w-12 text-2xl absolute top-0 right-0 md:hidden" @click.self="close">X</button>
                </div>
                <div class="w-full md:w-2/5 h-full bg-white px-5 md:px-6 lg:px-12 py-12 overflow-scroll">
                    <h1 class="text-xl font-bold">Essential Pack</h1>
                    <span class="text-2xl text-gray-700">₦7,000.00</span>
                    <h2 class="text-black text-l py-7 font-bold pl-12">518 sold in last 103 hours</h2>
                    <p class="font-bold text-gray-400">The perfect starter kit to get you on your cleaning journey. The pack contains a 100ml bottle of our Sneaker Cleaner gel, a Suede Dry-Cleaning Eraser and Standard Brush.</p>
                    <ul class="list-disc mt-8">
                        <li class="font-bold text-gray-400">Does not contain any harsh chemicals or abrasives</li>
                        <li class="font-bold text-gray-400 mt-2">Completely biodegradable</li>
                        <li class="font-bold text-gray-400 mt-2">Safe on all colors and materials (Apart from Suede & Nubuck)</li>
                        <li class="font-bold text-gray-400 mt-2">Effectively cleans and conditions</li>
                        <li class="font-bold text-gray-400 mt-2">Cleans up to 20 pairs of sneakers</li>
                        <li class="font-bold text-gray-400 mt-2">Standard brush is excellent for tackling dirt on midsoles</li>
                    </ul>
                    <div class="flex justify-between py-8">
                      <input type="number" class="pl-7 w-16 h-10 border border-black">
                      <button class="bg-blue-400 h-10 w-40 rounded-full text-white">ADD TO CART</button>
                      <button class="w-10 h-10 border border-black rounded-full">go</button>
                    </div>
                    <p class="font-bold text-gray-400 mb-3">SKU: N/A</p>
                    <p class="font-bold text-gray-400 mb-3">Categories: <a class="text-black">Home page</a>, <a class="text-black">Products</a></p>
                    <p class="font-bold text-gray-400 mb-3">Order in the next to get it between <span class="text-black underline"> Monday, 27th March</span> and <span class="text-black underline"> Monday, 27th March</span></p>
                    <button>View full details &#8594</button>
                </div>
            </div>
        </div>
</template>

<style scoped>
    .w{
        width: 65rem;
        height: 36.5rem;
    }
    .bg{
        background-color: rgba(0, 0, 0, 0.596);
    }
    .scroll{
        overflow-y: scroll;
    }
    p,li{
        font-size: 14px;
    }




    .fade-enter-active,
.fade-leave-active {
  transition: all 0.9s ease;
  overflow: hidden;
  visibility: visible;
  position: absolute;
  width:100%;
  opacity: 1;
}

.fade-enter,
.fade-leave-to {
  visibility: hidden;
  width:100%;
  opacity: 0;
}

img {
height:36.5rem;
width:100%
  }


/* On hover, add a black background color with a little bit see-through */
.prev:hover, .next:hover {
  background-color: rgba(0,0,0,0.9);
  color: white;
}
@media (max-width: 770px) {
  .w{
    width: 47.5rem;
    height: 30rem;
  }
  img{
    height: 30rem;
  }
}
@media (max-width: 380px) {
  .w{
    width: 22rem;
    height: 51rem;
  }
  img{
    height: 24rem;
  }
  .scroll{
        overflow-y: auto;
    }
    .rol{
      overflow-y: scroll;
    }
    .f{
      height: 50rem;
    }
}
</style>


<script>
export default {
  name: 'Slider',
  data() {
    return {
        images: [
        'https://cdn.shopify.com/s/files/1/0263/2430/3946/products/Untitleddesign_69338fff-a36a-4d07-ae57-3609143c5f02_1080x.png?v=1660228614',
        'https://cdn.shopify.com/s/files/1/0263/2430/3946/products/untitled162_1080x.jpg?v=1660230175',
        'https://cdn.shopify.com/s/files/1/0263/2430/3946/products/untitled11_1080x.jpg?v=1660230218',
        'https://cdn.shopify.com/s/files/1/0263/2430/3946/products/Untitleddesign_5_1080x.png?v=1662566225'
        ],
      timer: null,
      currentIndex: 0,
    }
  },

  
    mounted: function() {
      this.startSlide();
    },
  
    methods: {
      startSlide: function() {
        this.timer = setInterval(this.next, 5000000);
      },
  
  
      next: function() {
        this.currentIndex += 1
      },
      prev: function() {
        this.currentIndex -= 1
      },
      close() {
        this.$emit('close')
      }
    },
  
    computed: {
      currentImg: function() {
        return this.images[Math.abs(this.currentIndex) % this.images.length];
      }
  },
}
</script>

