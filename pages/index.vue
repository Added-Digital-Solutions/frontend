
<template>
  <Head>
    <Title>Home | Added Digital Solutions</Title>
  </Head>
  <CarouselsHero />
  <section class="max-w-7xl py-20 container mx-auto px-6 text-accent">
    <UiTypographyH2>we are added<span class="text-primary">.</span></UiTypographyH2>
    <UiTypographyP class="mt-6">We're a small collective of Award Winning Branding and Digital Marketing specialists with a passion for breathing new life into new and existing brands. Our team considers ourselves to be digital storytellers but the stories we're telling don't belong to us! <br /> <br />ADS gets to know your business inside and out, meeting your team, learning your history and goals and examining your needs to create memorable, stand-out branding that tells the story of your brand.<br /> <br />We're a full-service agency that specialises in branding, print, packaging, web design and digital advertising. Take the first steps and talk to a member of our team today!</UiTypographyP>
    
    <NuxtLink>
      <UiButtonsTalk class="text-primary hover:text-secondary duration-300 ease-in-out w-36 cursor-pointer mt-8" />
    </NuxtLink>
  </section>

  <section>
    <div class="bg-light text-accent">
      <div class="pt-20 pb-6 px-6 max-w-7xl container mx-auto block lg:flex gap-8">
        <UiTypographyH2 class="block min-w-fit mb-8">what we do<span class="text-primary">.</span></UiTypographyH2>
        <div>
          <UiTypographyP>We're an agency that won't bull***t you, let alone try to sell you something. We only recommend things that are in the interest of our clients, and we're here for long-term relationships, not quick wins. We have a “whatever it takes” attitude instilled in us to make sure that projects are serviced way above the required means, delivered on time and within the required deadline every time.<br /><br />The “designer” taking your brief will be responsible for working on the project so they receive the brief first hand (avoiding any loss in important communication), thus understanding the project far better than an account handler passing on the information third hand.<br /><br />At ADS we are proud to have built such a highly skilled and multi-disciplined team. Check out our disciplines overview below!</UiTypographyP>

          <div class="grid md:grid-cols-2 gap-8 mt-12">
            <div v-for="service in services" :key="service.id" class="services">
              <UiTypographyH2>{{ service.title }}</UiTypographyH2>
              <UiTypographyP class="mt-6">{{ service.description }}</UiTypographyP>
            </div>
          </div>
        </div>

      </div>
    </div>
    <img src="@/assets/images/triangle.svg" class="w-full abolute bottom-0" />
  </section>

  <section class="px-6 py-20 max-w-7xl container mx-auto text-accent">
    <UiTypographyH2>check out some of our work<span class="text-primary">.</span></UiTypographyH2>
    <UiTypographyP class="mt-2">Interested in our work? Check out some of the brand stories we've helped to create. </UiTypographyP>

      <ul class="mt-8 grid md:grid-cols-3 gap-8">
        <li v-for="project in projects" :key="project.id">
          <div :style="{ background:`url(${project.imagePath})`}" class="background w-full aspect-square bg-accent"></div>
        </li>
      </ul>
    </section>

  <CarouselsReviews />

  <section class="max-w-7xl container mx-auto py-20 px-6 text-center text-accent">
    <UiTypographyH2>some of our happy clients</UiTypographyH2>
    <ul class="mt-16 grid grid-cols-2 md:grid-cols-4 gap-8 xl:gap-16 place-items-center" >
      <li v-for="image in brands" :key="image.id">
        <img :src="image.image" class="w-40 mx-auto" alt="">
      </li>
    </ul>
  </section>
</template>
<script>
import tb from '@/assets/brand/clients/tb.svg'
import niffy from '@/assets/brand/clients/niffy.svg'
import vacations from '@/assets/brand/clients/vacations.svg'
import naked from '@/assets/brand/clients/naked.svg'
import one from '@/assets/brand/clients/oneonone.svg'
import ajwaad from '@/assets/brand/clients/ajwaad.svg'
import exclusive from '@/assets/brand/clients/exclusive.svg'
import williams from '@/assets/brand/clients/williams.svg'

import image1 from '@/assets/brand/projects/01.jpg';
import image2 from '@/assets/brand/projects/02.jpg';
import image3 from '@/assets/brand/projects/03.jpg';
export default {
  data() {
    return {
      services: [
        {
          id: 1,
          title: 'branding & positioning',
          description: `We've worked with businesses on an International level to create memorable product branding, logos, printed materials and more.`,
        },
        {
          id: 2,
          title: 'digital & online',
          description: `Our branding doesn't stop at the supermarket shelves, we design and build fully responsive, mobile-friendly websites that allow you to truly showcase your brand!`,
        },
        {
          id: 3,
          title: 'packaging & instore',
          description: 'Packaging and in-store advertising is the first thing your customers will see when searching for new products. Make your brand memorable with our expert product designs.',
        },
        {
          id: 4,
          title: 'marketing & advertising',
          description: 'Quality marketing and advertising creates engagement for your brand. Sourcefour specialise in Digital Marketing, Search Engine Optimisation (SEO) and Pay Per Click advertising',
        },
      ],
      brands:[
        {
          id: 1,
          image: tb
        },
        {
          id: 2,
          image: niffy
        },
        {
          id: 3,
          image: vacations
        },
        {
          id: 4,
          image: naked
        },
        {
          id: 5,
          image: williams
        },
        {
          id: 6,
          image: one
        },
        {
          id: 7,
          image: ajwaad
        },
        {
          id: 8,
          image: exclusive
        },
      ],
      projects: [
        {
          id: 1,
          imagePath: image1
        },
        {
          id: 2,
          imagePath: image2
        },
        {
          id: 3,
          imagePath: image3
        },
      ]
    }
  },
}
</script>
<style>
.services:first-child>h2{
  color: #058182;
}
.services:last-child>h2{
  color: #058182;
}
.background {
  background-size: cover !important;
  background-position: center !important;
  background-repeat: no-repeat !important;
}
</style>