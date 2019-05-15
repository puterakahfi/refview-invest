<template>
  <div class="container">
    <div class="columns align-items-center">
      <div class="column is-7">
        <section class="hero is-marginless">
          <div class="hero-body">
            <div class="titleunderline"></div>

            <h1>Kode referal</h1>
            <h2
              class="subtitle"
            >Gunakan kode referal ketika mendaftar untuk mendapatkan berbagai penawaran menarik</h2>
          </div>
        </section>

        <br>
      </div>
      <div class="column is-5">
        <figure class="image">
          <img
            src="https://42f2671d685f51e10fc6-b9fcecea3e50b3b59bdc28dead054ebc.ssl.cf5.rackcdn.com/illustrations/mobile_app_0irr.svg"
            alt="Placeholder image"
          >
        </figure>
      </div>
    </div>

    <div class="columns is-multiline">
      <div class="column is-4">
        <nav class="level">
          <div class="level-item has-text-left">
            <div>

              <div class="titleunderline is-small"></div>
              <p class="heading">IGrow</p>
              <p class="title is-2">{{igrow[Math.floor(Math.random() * igrow.length)]}}</p>
            </div>
          </div>
        </nav>
      </div>
      <div class="column is-4">
        <nav class="level">
          <div class="level-item has-text-left">
            <div>

              <div class="titleunderline is-small"></div>
              <p class="heading">Investree</p>
              <p class="title is-2">{{investree[Math.floor(Math.random() * investree.length)]}}</p>
            </div>
          </div>
        </nav>
      </div>

      <div class="column is-4">
        <nav class="level">
          <div class="level-item has-text-left">
            <div>
              <div class="titleunderline is-small"></div>
              <p class="heading">Tanifund</p>
              <p class="title is-2">{{tanifund[Math.floor(Math.random() * tanifund.length)]}}</p>
            </div>
          </div>
        </nav>
      </div>
    </div>
  </div>
</template>

 <style lang="scss" scoped>
.level {
  position: relative;
  display: flex;
  overflow: hidden;
  flex-direction: row;
  justify-content: flex-start;
  flex-wrap: nowrap;
  align-items: flex-start;
  border: 1px none #e6ecf1;
  border-radius: 6px;
  background-color: #fff;
  border: none;
  transition: all 0.2s ease-in-out;
  box-shadow: none;
  padding: 1rem;

  &:hover {
    box-shadow: 0 2px 8px 0 rgba(0, 0, 0, 0.04),
      0 2px 20px 0 rgba(0, 0, 0, 0.06);
    transform: scale(1.1);
  }
}
</style>

<script>
export default {
  data() {
    return {
      igrow: ["IGWAKH1982", "IGWSAN1978", "IGWNAS1980"],
      tanifund: ["7301542"],
      investree: ["NKBFL"]
    };
  }
};
</script>
