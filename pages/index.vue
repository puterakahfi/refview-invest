<template>
  <div class="container">
    <div class="columns align-items-center">
      <div class="column is-7">
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
                <br>
              </div>

              <div class>
                <nuxt-link :to="'/platform/'+item.id">
                  <p class="title is-4">{{ item.title }}</p>
                </nuxt-link>
                <div class="titleunderline"></div>

                <section>
                  <b-tag>{{ item.tags }}</b-tag>
                </section>

                <br>
                <span v-if="typeof item.links !== 'undefined'">
                  <span :key="link.url" v-for="link in item.links">
                    <a :href="link.url" target="_blank">
                      <fa :icon="[link.icon.category, link.icon.icon]" class="fa-1x"/>&nbsp;
                    </a>
                  </span>
                </span>
                <hr class="is-paddingless">
                <div class="control">
                  <b-taglist attached class="rating">
                    <b-tag type="is-success"><b>rating</b></b-tag>
                    <b-tag type="is-dark">
                      <fa :icon="['fas', 'star']" class="has-text-warning"/>
                      <fa :icon="['fas', 'star']" class="has-text-warning"/>

                      <fa :icon="['fas', 'star']" class="has-text-warning"/>&nbsp;
                      <b>3.5</b> / 5
                    </b-tag>
                  </b-taglist>
                </div>
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
.tags.has-addons .tag {
  font-size: .6em;
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
