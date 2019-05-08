<template>
  <div class="container">
    <div class="columns align-items-center">
      <div class="column is-7">
        <h1>REVIEW PLATFROM INVESTASI</h1>
        <p
          class="lead"
        >Refview berbagai platform investasi berdasarkan pengalaman dari para lender dari group whatsapp, refview di aplikasi, blog, etc</p>

        <br>

        <div class="cta">
          <b>
            <a
              class="button is-primary shadowless"
              href="https://goo.gl/forms/72OsZ6lTMde84YkO2"
              target="_blank"
            >
              <fa :icon="['fab', 'whatsapp']" class="fa-lg"/>&nbsp;Daftar di group wa agri invest
            </a>
          </b>
        </div>
      </div>
      <div class="column is-5"></div>
    </div>
    <br>
    <br>

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
                <a :href="item.url">
                  <p class="title is-3">{{ item.title }}</p>
                </a>

                <a href>
                  <fa :icon="['fab', 'instagram']" class="fa-lg"/>
                </a>
                <a href>
                  <fa :icon="['fab', 'facebook']" class="fa-lg"/>
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
