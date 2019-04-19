<template>
  <div class="container mt-5">
    <div class="row align-items-center">
      <div class="col-7">
        <h1>REVIEW PLATFROM INVESTASI</h1>
        <p
          class="lead"
        >Refview berbagai platform investasi berdasarkan pengalaman dari para lender dari group whatsapp, refview di aplikasi, blog, etc</p>
        <div class="cta">
          <b>
            <a
              class="btn btn-lg btn-primary btn-icon icon-right shadowless"
              href="https://goo.gl/forms/72OsZ6lTMde84YkO2"
              target="_blank"
            >
              <fa :icon="['fab', 'whatsapp']" class="fa-lg"/>&nbsp;Daftar di group wa agri invest
            </a>
          </b>
        </div>
        <div class="col-5"></div>
      </div>
    </div>

    <div class="row mt-5 pt-5">
      <div class="col-md-12">
        <div class="row">
          <div class="col">

            
            <div class="card">
              <div class="card-header">
                <h4>Crowde</h4>
              </div>
              <div class="card-body">This is some text within a card body.</div>
              <div class="card-footer">Footer Card</div>
            </div>
          </div>
          <div class="col">
            <div class="card">
              <div class="card-header">
                <h4>IGrow</h4>
              </div>
              <div class="card-body">This is some text within a card body.</div>
              <div class="card-footer">Footer Card</div>
            </div>
          </div>
          <div class="col">
            <div class="card">
              <div class="card-header">
                <h4>Growpal</h4>
              </div>
              <div class="card-body">This is some text within a card body.</div>
              <div class="card-footer">Footer Card</div>
            </div>
          </div>
        </div>
      </div>

         <div class="col-md-12">
        <div class="row">
          <div class="col">
            <div class="card">
              <div class="card-header">
                <h4>Tanijoy</h4>
              </div>
              <div class="card-body">This is some text within a card body.</div>
              <div class="card-footer">Footer Card</div>
            </div>
          </div>
          <div class="col">
            <div class="card">
              <div class="card-header">
                <h4>Ammana</h4>
              </div>
              <div class="card-body">This is some text within a card body.</div>
              <div class="card-footer">Footer Card</div>
            </div>
          </div>
          <div class="col">
            <div class="card">
              <div class="card-header">
                <h4>Tanihub</h4>
              </div>
              <div class="card-body">This is some text within a card body.</div>
              <div class="card-footer">Footer Card</div>
            </div>
          </div>
        </div>
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
