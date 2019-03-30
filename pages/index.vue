<template>
  <div class="hero-mini bg">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-7">
          <h1>REVIEW PLATFROM INVESTASI</h1>
          <p
            class="lead"
          >Refview berbagai platform investasi berdasarkan pengalaman dari para lender dari group whatsapp, refview di aplikasi, blog, etc</p>
          <div class="cta">
            <a
              class="btn btn-lg btn-primary btn-icon icon-right shadowless"
              href="https://goo.gl/forms/72OsZ6lTMde84YkO2"
              target="_blank"
            >
              <fa :icon="['fab', 'whatsapp']" class="fa-lg"/> Daftar di group wa agri invest
            </a>
          </div>
        </div>
        <div class="col-5"></div>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";

export default {
  components: {
    Logo
  }
};
</script>

<style sccoped>

.btn.btn-lg {
    padding: .55rem 1.5rem;
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
