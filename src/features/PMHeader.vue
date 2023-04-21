<template>
  <div>
    <section class="cbs-header">
      <div class="container">
        <img
          src="../assets/images/CBS/census_logo-light.png"
          alt="Census Logo"
        />
        <div class="content">
          <!-- Divider between logo and App title -->
          <div class="divider"></div>
          <div class="header-text">
            <h1>{{ title }} - {{ role }}</h1>
            <p>{{ subTitle }}</p>
          </div>
        </div>
      </div>

      <img src="../assets/images/CBS/census_header.jpg" alt="Building Image" />
    </section>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  name: "CBSHeader",
  props: {
    title: {
      type: String,
      required: true,
    },
    role: {
      type: String,
      required: false,
    },
    subTitle: {
      type: String,
      required: false,
    },
    dropdownList: {
      type: Array,
      required: false,
      default: () => [],
    },
  },
  computed: {
    myRole: {
      get: function () {
        return this.role;
      },
      set: function (value) {
        this.$emit("role-change", value);
      },
    },
  },
};
</script>

<style lang="scss">
@import "../colors.module";
.page-padding {
  padding: 1.7em 1.8em 3.5em 1.8em;
}

.cbs-header-banner {
  background: #323a45;
  text-align: right;
  height: 35px;
  line-height: 35px;
  padding: 1px 10px 0px 0px;

  p {
    margin: 0;
    color: $primary-white;
    font-size: 17px;
    font-weight: 400;
  }
}

//////////////////////////////////////////////////////////////////////////////
// Header.vue

.cbs-header {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-orient: horizontal;
  -webkit-box-direction: normal;
  -ms-flex-direction: row;
  flex-direction: row;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
  background-color: $primary;
  height: 105px;

  .container {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;

    > img {
      width: 158px;
      height: 57px;
      margin-left: 30px;
      margin-top: -2px;
      //margin-top: 23px;
    }
  }

  > img:nth-child(2) {
    width: 27%;
  }
}

.content {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;

  .divider {
    width: 0;
    border-right: 1px solid #e3e6f0;
    height: calc(5.2rem - 1rem);
    margin: auto 1rem;
    padding-left: 16px;
  }

  .header-text {
    -ms-flex-direction: column;
    box-orient: vertical;
    box-direction: normal;
    flex-direction: column;
    line-height: 1;
    margin-top: 6px;

    h1,
    p {
      color: white;
    }

    h1 {
      margin-top: 5px;
      font-size: 37px;
      margin-bottom: 0px;
      font-weight: 400;
    }

    p {
      margin-top: 2px;
      margin-bottom: 10px;
      font-size: 19px;
    }
  }
}
</style>
