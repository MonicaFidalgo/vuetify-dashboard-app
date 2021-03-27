<template>
  <v-footer padless>
    <v-card flat tile width="100%" class="text-center">
      
      <v-card-text class="footer-links">
        <div v-for="(link,idx) in links" :key="idx">
          <v-btn
            text
            rounded
            class="my-2"
            v-if="!link.image"
          >
            {{ link.name }}
          </v-btn>
          <span v-else>
          <img :src="require(`../assets/${link.imageFile}.png`)" class="footer__logo" />
          </span>
        </div>
      </v-card-text>

      <v-divider></v-divider>
      <div class="o-separator--variant1"></div>
      <div class="o-separator--variant1"></div>
      <v-card-text>
        <a v-bind:href="social.url" v-for="(social, id) in socials" :key="id" >
          <v-btn class="mx-4" icon>
             <img :src="require(`../assets/icons/${social.name}.png`)" style="width: 40px; height: 40px" />
          </v-btn>
        </a> 
      </v-card-text>

      <v-card-text>
        @ Dash.io {{ new Date().getFullYear() }}. We love our users!
      </v-card-text>
    </v-card>

  </v-footer>
</template>

<script>

export default {
    name: 'Footer',
    data: () => ({
      panel: [],
      links: [
        {
          name: 'Community'
        },
        {
          name: 'Company'
        },
        {
          name: 'logo',
          image: true,
          imageFile: 'Dash.io'
        },
        {
          name: 'Help desk'
        },
        {
          name: 'Blog'
        },
      ],
      socials: [
        {
          name:"linkedin",
          icon:"mdi-linkedin",
          url:"#!"
          },
        {
          name:"facebook",
          icon:"mdi-facebook",
          url:"#!"
        },
        {
          name:"twitter",
          icon:"mdi-twitter",
          url:"#!"
        },
        {
          name:"youtube",
          icon:"mdi-youtube",
          url:"#!"
        }
      ],
      items: [
        {
          name: "Product",
          tags: [
            {
              urlname: "Create Websites",
              url: "#!"
            },
            {
              urlname: "Secure Cloud Hosting",
              url: "#!"
            },
            {
              urlname: "Engage Your Audience",
              url: "#!"
            },
            {
              urlname: "Website Support",
              url: "#!"
            }
          ]
        },
        { 
          name: "Company", 
          tags: [
            { urlname: "About", url: "#!" },
            { urlname: "Careers", url: "#!"},
            { urlname: "Support", url: "#!"},
            { urlname: "Pricing", url: "#!"},
            { urlname: "FAQ", url: "#!"}
          ] 
        },
        { 
          name: "Resources", 
          tags: [
            { urlname: "Blog", url: "#!" },
            { urlname: "eBooks", url: "#!" },
            { urlname: "Whitepapers", url: "#!" },
            { urlname: "Comparison Guide", url: "#!" },
            { urlname: "Website Grader", url: "#!" }
          ] 
        },
        { 
          name: "Get Help", 
          tags: [
            { urlname: "Help Center", url: "#!" },
            { urlname: "Contact Us", url: "#!" },
            { urlname: "Privacy Policy", url: "#!" },
            { urlname: "Terms", url: "#!" },
            { urlname: "Login", url: "#!" }
          ]
        }
      ]
  }),
}
</script>
