<template>
  <div @scroll="handleScroll">
    <div class="position-relative background-css" v-if="isVisible">
      <div
        class="position-absolute top-50 end-0 translate-middle-y bg-white p-3 me-5 protection-box"
      >
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
        <div class="mb-2 fs-5">
          <span class="fw-bold">All-in-one</span>
          protection
        </div>
        <p class="fs-8">
          Online protection for your identity, privacy, and devices, includes
          antivirus, VPN, and Protection Score.
          <span class="fw-bold">Family plans are now available.</span>
        </p>
        <div class="d-flex my-3 align-items-center">
          <button
            class="btn btn-danger fs-8 me-4"
            style="border-radius: 40px"
            type="submit"
          >
            Get protection now
          </button>
          <button
            class="btn border fs-8 me-4 px-3"
            style="border-radius: 40px"
            type="submit"
          >
            Compare plans
          </button>
        </div>
      </div>
    </div>
    <div class="position-relative background-css2" v-else>
      <div
        class="position-absolute top-50 end-0 translate-middle-y p-2 ps-3 me-5 protection-box2"
      >
        <div class="mb-2 fs-5 fw-bolder">All-in-one protection</div>
        <p class="fs-8">
          Online protection for your identity, privacy, and devices, includes
          antivirus, VPN, and Protection Score.
          <span class="fw-bold">Family plans are now available.</span>
        </p>
        <div>$49.99* <span class="fs-8">/yr</span></div>
        <div class="fs-7">
          <span class="text-decoration-line-through text-secondary me-1"
            >$149.99 </span
          ><span class="text-danger">(Save $100)</span>
        </div>
        <div class="d-flex my-3 align-items-center">
          <button
            class="btn btn-danger fs-8 me-2"
            style="border-radius: 40px"
            type="submit"
          >
            Get protection now
          </button>
          <button
            class="btn border fs-8 me-4 px-3"
            style="border-radius: 40px"
            type="submit"
          >
            See plans
          </button>
        </div>
      </div>
    </div>
    <div style="height: 50vh"></div>
  </div>
</template> 
<script>
export default {
  name: "ThirdSection",
  data() {
    return {
      isVisible: true,
    };
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      if (window.scrollY > 850) {
        this.isVisible = false;
      } else {
        this.isVisible = true;
      }
    },
  },
};
</script>