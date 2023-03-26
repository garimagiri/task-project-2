<template>
  <div class="m-5">
    <div class="row">
      <div class="col-sm-1 mt-5">
        <div class="row mb-3">
          <div class="symbol symbol-45px">
            <img src="../assets/150-10.jpg" alt="" />
          </div>
        </div>
        <div class="row mb-3">
          <div class="symbol symbol-45px">
            <img src="../assets/150-14.jpg" alt="" />
          </div>
        </div>
        <div class="row mb-3">
          <div class="symbol symbol-45px">
            <img src="../assets/150-16.jpg" alt="" />
          </div>
        </div>
        <div class="row mb-3">
          <div class="symbol symbol-45px">
            <img src="../assets/150-20.jpg" alt="" />
          </div>
        </div>
        <div class="row mb-3">
          <div class="symbol symbol-45px">
            <img src="../assets/150-7.jpg" alt="" />
          </div>
        </div>
      </div>
      <div class="col-sm-5">
        <img
          :src="image"
          alt=""
          class="w-100 h-75 rounded"
        />
      </div>
      <div class="col-sm-6 ps-5">
        <div class="fs-9">
          <span class="badge bg-danger me-2">New</span
          ><span class="fw-bold">Introducing</span>
        </div>
        <div>
          <img
            src="../assets/mcafee_logo.svg"
            alt="logo"
            width="100"
            height="50"
          /><span class="fw-bold">+</span>
        </div>
        <div class="fs-3 lh-sm mb-2 me-5">
          Identity <span class="fw-bold">protection</span> and
          <span class="fw-bold">privacy </span>for your digital life
        </div>
        <div>
          <div class="me-5">
            <ul class="nav nav-tabs nav-justified">
              <li class="nav-item">
                <a
                  class="nav-link active"
                  data-bs-toggle="tab"
                  href="#kt_tab_pane_1" @click="getImage1()"
                  >Individual</a
                >
              </li>
              <li class="nav-item">
                <a class="nav-link" data-bs-toggle="tab" @click="getImage()" href="#kt_tab_pane_2"
                  >Family</a
                >
              </li>
            </ul>
          </div>
          <div class="tab-content mt-4" id="myTabContent">
            <div
              class="tab-pane fade show active"
              id="kt_tab_pane_1"
              role="tabpanel"
              aria-labelledby="kt_tab_pane_1"
            >
              <IndividualTab />
            </div>
            <div
              class="tab-pane fade"
              id="kt_tab_pane_2"
              role="tabpanel"
              aria-labelledby="kt_tab_pane_2"
            >
              <FamilyTab />
            </div>
          </div>
        </div>
        <div class="d-flex my-4 align-items-center">
          <button
            class="btn btn-danger px-4 me-4"
            style="border-radius: 40px"
            type="submit"
          >
            Get protection now
          </button>
          <a href="#" class="">See more plans below</a>
        </div>
        <p class="fs-9">
          Introductory pricing for new customers. *First year price.
          <a href="" class="text-secondary">See offer details</a>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import IndividualTab from "./IndividualTab.vue";
import FamilyTab from "./FamilyTab.vue";
export default {
  name: "MainComponent",
  components: {
    IndividualTab,
    FamilyTab,
  },
  data(){
    return{
        image : require('../assets/demo_image_1.jpg'),
        
    }
  },
  methods: {
    getImage(){
        this.image = require('../assets/demo_image_2.jpg');
    },
    getImage1(){
       this.image = require('../assets/demo_image_1.jpg');
    }
  }
};
</script>