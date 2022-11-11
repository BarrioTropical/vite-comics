<template>
    <main>
    <section class="content">
        <div class="row"> 
            <div class="product" v-for="(item, index) in products" :key="index" >
                <img :src="item.thumb">
                <h3>{{item.series}}</h3>
            </div>
        </div>


        <button class="btn">load more</button>
    </section>

    <section class="merch">
        <div class="flex container">
        <ul class="flex">

            <li v-for="(data, index) in data" :key="index">
                <div class="flex">
                <img :src="data.url" alt="">
                <h4>{{ data.text }}</h4>
                </div>  
            </li>
        </ul>
        </div>
    </section>

    </main>
</template>

<script>
    export default {
        name: 'MainComponent',

        data() {
            return {
                data: [
                {
                    text: "Digital Comics",
                    url: "../assets/img/buy-comics-digital-comics.png",
                },
                {
                    text: "Dc Merchandise",
                    url: "../assets/img/buy-comics-merchandise.png",
                },
                {
                    text: "Scubscription",
                    url: "../assets/img/buy-comics-scubscriptions.png",
                },
                {
                    text: "Comic Shop Locator",
                    url: "../assets/img/buy-comics-shop-locator.png",
                },
                {
                    text: "Dc Power Visa",
                    url: "../assets/img/buy-dc-power-visa.png",
                },
                ],

                products: [
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel"
                }
                ],
            }
        },  
        methods: {
            getImagePath(imgPath){
                return new URL(imgPath, import.meta.url).href;
            }
        },

    }
</script>

<style lang="scss" scoped>
    @use '../assets/styles/partials/variables' as *;
    @use '../assets/styles/partials/mixins' as *;
    @use '../assets/styles/generals.scss' as *;

    .content{
        background-color: $greydark;
        color: $white;
    }

    .merch{
        background-color: $blue;
        color: $white;
    }
    img{
        max-width: 100px;
    }

    section{
        padding: 20px;
    }

    .flex {
        display: flex;  
        justify-content: space-around;
        vertical-align: middle;
    }

    .flex-product{
        display: flex;  
        justify-content: space-around;
        vertical-align: middle;
    }

    ul{

        vertical-align: middle;

        li{
            list-style: none;
            padding: 10px;
        }

        h4{
            text-transform: uppercase;
            padding: 3px;
            font-size: 15px;
        }

 

        
    }


    .btn{
            background-color: $blue;
            text-align: center;
            padding: 15px 50px;
            color: $white;
            text-transform: uppercase;
            font-weight: bold;
            font-size: 15px;
        }

    .row{
            display: flex;
            justify-content: center;
            flex-flow: row nowrap;
            align-items: center;

       }

       .product{
            margin-top: 30px;
            width: calc(100%/6);
           

            h3{
                margin-top: 5px;
            }
        }
</style>