<template>
  <div class="container">
    <div class="columns align-items-center">
      <div class="column is-7">
        <section class="hero is-marginless">
          <div class="hero-body">
            <div class="titleunderline"></div>
            <h1 class="title is-1">Review Platform Investasi</h1>
            <p class="subtitle is-6">
              Refview berbagai platform investasi
              berdasarkan pengalaman dari para lender dari group whatsapp, refview di aplikasi, blog, etc
              <br>
            </p>

            <br>
            <div class="cta">
              <a
                class="button is-info is-normal shadowless"
                href="https://goo.gl/forms/72OsZ6lTMde84YkO2"
                target="_blank"
              >
                <fa :icon="['fab', 'whatsapp']" class="fa-1x"/>&nbsp;daftar wa group agri invest
              </a>
              <a
                class="button is-success is-normal shadowless"
                href="/docs/fintechOJK.xlsx"
                target="_blank"
              >
                <fa :icon="['fas', 'download']" class="fa-1x"/>&nbsp;fintecth yg terdaftar di OJK
              </a>
            </div>
          </div>
        </section>
      </div>
      <div class="column is-5">
        <figure class="image">
          <img
            src="https://42f2671d685f51e10fc6-b9fcecea3e50b3b59bdc28dead054ebc.ssl.cf5.rackcdn.com/illustrations/finance_0bdk.svg"
            alt="Placeholder image"
          >
        </figure>
      </div>
    </div>
    <div class="columns is-multiline mt-5 pt-5">
      <div class="column is-4" v-for="item in data" :key="item.id">
        <div class="card has-equal-height">
          <div class="card-content">
            <div class="media">
              <div class="media-left">
                <figure class="image is-128x128">
                  <img :src="item.image" alt="Placeholder image">
                </figure>
              </div>
              <div class="media-content">
                <nuxt-link :to="'/platform/'+item.id">
                  <p class="title is-4">{{ item.title }}</p>
                </nuxt-link>

                <div class="titleunderline"></div>

                <section>
                  <b-tag>{{ item.tags }}</b-tag>
                </section>

                <br>
                <a href>
                  <fa :icon="['fab', 'instagram']" class="fa-1x"/>
                </a>
                <a href>
                  <fa :icon="['fab', 'facebook']" class="fa-1x"/>
                </a>
                <a href>
                  <fa :icon="['fab', 'twitter']" class="fa-1x"/>
                </a>
              </div>
            </div>

            <div class="content">{{ item.description }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";
import data from "~/static/data/platforms.json"; // Or wherever it is found

export default {
  data() {
    return {
      data: data
    };
  },
  components: {
    Logo
  }
};
</script>

<style sccoped>
.btn.btn-lg {
  padding: 0.55rem 1.5rem;
  font-size: 14px;
}

h1 {
  font-size: 3rem;
  font-weight: 800;
}

.btn-wa {
  background: #77cb6a;
}
.hero-mini {
  background-image: #ededed;
  padding-top: 40px;
  height: 500px;
  display: flex;
  align-items: center;
}
</style>
