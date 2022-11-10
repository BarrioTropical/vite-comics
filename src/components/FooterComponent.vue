<template>
    <footer>
    <div class="container flex">
    <div class="flex">
        <div>
    <h3>Dc</h3>
    <ul>
        <li v-for="(menu, index) in menu" :key="index">
            <a :href="menu.url" :class="{ 'active': menu.current }">{{ menu.text }}</a>
        </li>
    </ul>

    <h3>Shop</h3>
    <ul>
        <li v-for="(shop, index) in shop" :key="index">
            <a :href="shop.url" :class="{ 'active': shop.current }">{{ shop.text }}</a>
        </li>
    </ul>
    
    </div>

    <div>
        <h3>Dc Comics</h3>
    <ul>
        <li v-for="(dc, index) in dc" :key="index">
                    <a :href="dc.url" :class="{ 'active': dc.current }">{{ dc.text }}</a>
        </li>
    </ul>
    </div>

    <div>
        <h3>Sites</h3>
    <ul>
        <li v-for="(sites, index) in sites" :key="index">
                    <a :href="sites.url" :class="{ 'active': sites.current }">{{ sites.text }}</a>
        </li>
    </ul>
    </div>
    
    </div>
    
    <div class="img-footer">
    <img src="../assets/img/dc-logo-bg.png" alt="">
    </div>
    </div>
    </footer>
    <div class="subfooter">
    <div class=" container flex">
    <button>Sign-up Now!</button>
    
    <div>
    <div class="flex">
    <div><h4>Follow us</h4></div>
    </div>
    
    </div>

    </div>
    </div>  
</template>

<script>
    export default {
        name: 'FooterComponent',
        data() {
            return {
                menu: [
                {
                    text: "Characters",
                    url: "#",
                    current: false,
                },
                {
                    text: "Comics",
                    url: "#",
                    current: true,
                },
                {
                    text: "Movies",
                    url: "#",
                    current: false,
                },
                {
                    text: "Tv",
                    url: "#",
                    current: false,
                },
                {
                    text: "Games",
                    url: "#",
                    current: false,
                },
                {
                    text: "Collectibles",
                    url: "#",
                    current: false,
                },
                {
                    text: "Videos",
                    url: "#",
                    current: false,
                },
                {
                    text: "Fans",
                    url: "#",
                    current: false,
                },
                {
                    text: "News",
                    url: "#",
                    current: false,
                },
                ],
                shop: [
                {
                    text: "Shop DC",
                    url: "#",
                    current: false,
                },
                {
                    text: "Shop DC COllectibles",
                    url: "#",
                    current: true,
                },
                ],
                sites: [
                {
                    text: "DC",
                    url: "#",
                    current: false,
                },
                {
                    text: "MAD Magazine",
                    url: "#",
                    current: true,
                },
                {
                    text: "DC Kids",
                    url: "#",
                    current: true,
                },
                {
                    text: "DC Universe",
                    url: "#",
                    current: true,
                },
                {
                    text: "DC Power Visa",
                    url: "#",
                    current: true,
                },
                ],
                dc: [
                {
                    text: "Ad Choices",
                    url: "#",
                    current: false,
                },
                {
                    text: "Advertising",
                    url: "#",
                    current: true,
                },
                {
                    text: "Jobs",
                    url: "#",
                    current: true,
                },
                {
                    text: "Subscriptions",
                    url: "#",
                    current: true,
                },
                {
                    text: "Talent Workshops",
                    url: "#",
                    current: true,
                },
                {
                    text: "CPSC Certifications",
                    url: "#",
                    current: true,
                },
                {
                    text: "Ratings",
                    url: "#",
                    current: true,
                },
                {
                    text: "Shop Help",
                    url: "#",
                    current: true,
                },
                {
                    text: "Contact Us",
                    url: "#",
                    current: true,
                },
                ]
            }
        },  
    }
</script>

<style lang="scss" scoped>
    @use '../assets/styles/partials/variables' as *;
    @use '../assets/styles/partials/mixins' as *;
    @use '../assets/styles/generals.scss' as *;

    footer{
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
        background-repeat: no-repeat;
        color: white;

        h3{
            text-transform: uppercase;
            padding: 1rem 0rem;
        }

        ul{
            text-decoration: none;
            list-style: none;
        
            li{
            text-decoration: none;
        }


        li a{
            color: grey;
            text-decoration: none;
            list-style: none;

        }
    }
    }

    .img-footer{
        max-width: 300px;
    }


    .subfooter{
        background-color: $greylight;

        button{
            border: 1px solid $blue;
            padding: 1rem;
            background-color: transparent;
            color: $white;
            text-transform: uppercase;
        }

        h4{
            color: $white;
            text-transform: uppercase;
        }

    }

</style>