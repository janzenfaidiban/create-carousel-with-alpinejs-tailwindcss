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