# Tutorial

    Fitur Carousel Menggunakan Tailwindcss & Alpine.js by Ferry Dermawan
    https://youtu.be/WKrDeWeasE8

## Demo
https://janzenfaidiban.github.io/create-carousel-with-alpinejs-tailwindcss/

## Screenshot

![alt text](https://raw.githubusercontent.com/janzenfaidiban/create-carousel-with-alpinejs-tailwindcss/main/screenshoot.png)



## Membuat Data

    x-data="{
        activeSlide: 3,

        slides: [
        {id:1, title: 'Hello 1', body: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam, esse!'},
        {id:2, title: 'Hello 2', body: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, quisquam fugiat maxime aliquam consequuntur dignissimos nostrum quae debitis quasi eos.'},
        {id:3, title: 'Hello 3', body: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam, esse!'},
        {id:4, title: 'Hello 4', body: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, quisquam fugiat maxime aliquam consequuntur dignissimos nostrum quae debitis quasi eos.'},
        {id:5, title: 'Hello 5', body: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam, esse!'},
        ],

        loop() {
            setInterval(() => {this.activeSlide = this.activeSlide === 5 ? 1 : this.activeSlide + 1}, 2000)
        }
        
    }"

## Tombol Back

    <div class="flex items-center justify-start w-1/2">
        <button x-on:click="activeSlide = activeSlide === 1 ? slides.length : activeSlide - 1"
            class="bg-slate-100 text-slate-500 transition hover:text-white hover:bg-blue-500 font-bold rounded-full w-12 h-12 flex justify-center shadow items-center -ml-16">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
                stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M15 19l-7-7 7-7" />
            </svg>
        </button>
    </div>

## Tombol Next
                
    `<div class="flex items-center justify-end w-1/2">
        <button x-on:click="activeSlide = activeSlide === slides.length ? 1 : activeSlide + 1"
            class="bg-slate-100 text-slate-500 transition hover:text-white hover:bg-blue-500 font-bold rounded-full w-12 h-12 flex justify-center shadow items-center -mr-16">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
                stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M9 5l7 7-7 7" />
            </svg>
        </button>
    </div>`