<template>
  <div class="container">
    <div class="columns align-items-center">
      <div class="column is-6">
        <section class="hero is-marginless">
          <div class="hero-body">
            <div class="titleunderline"></div>

            <h1 class="title is-1">Review platform investasi</h1>

            <p class="subtitle is-6">
              Refview berbagai platform investasi
              berdasarkan pengalaman dari para lender dari group whatsapp,
              refview di aplikasi, blog, etc
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
      <div class="column is-6">
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
                <figure class="image is-96x96">
                  <img :src="item.image" alt="Placeholder image">
                </figure>
              </div>
              <div class="media-content">
                <div class="titleunderline is-marginless"></div>

                <nuxt-link :to="'/platform/'+item.id">
                  <p class="title is-3">{{ item.title }}</p>
                </nuxt-link>

                <div class="control">
                  <b-taglist attached class="rating">
                    <b-tag type="is-dark">
                      <fa :icon="['fas', 'star']" class="has-text-warning"/>
                      <fa :icon="['fas', 'star']" class="has-text-warning"/>

                      <fa :icon="['fas', 'star']" class="has-text-warning"/>&nbsp;
                      <b>3.5</b> / 5
                    </b-tag>
                  </b-taglist>
                </div>
              </div>
            </div> <br>
            <div class="content">
              <p class="subtitle is-size-6">{{ item.description }}</p>

              <section>
                <b-tag>{{ item.tags }}</b-tag>
              </section>

              <br>

              <p class="subtitle is-5">
                <span v-if="typeof item.links !== 'undefined'">
                  <span :key="link.url" v-for="link in item.links">
                    <a :href="link.url" target="_blank">
                      <fa :icon="[link.icon.category, link.icon.icon]" class="fa-1x"/>&nbsp;
                    </a>
                  </span>
                </span>
              </p>
            </div>
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
.tags.has-addons .tag {
  font-size: 0.6em;
  margin: 2px;
}
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
