<template>
  <div>
    <div
      class="py-10 bg-[#F9F9FB] h-[100%] min-h-screen px-4 sm:px-8 md:px-20 lg:px-[120px]"
    >
      <div
        class="flex flex-row justify-between items-start sm:items-center gap-4 sm:gap-0 rounded-lg"
      >
        <h1 class="text-lg sm:text-xl font-bold text-center sm:text-left">
          Misuse of Election Symbols
        </h1>

        <div class="rounded bg-[#0F75BC]">
          <div class="flex justify-center items-center ml-4">
            <svg
              width="20"
              height="21"
              viewBox="0 0 20 21"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M6.66699 14.6669H13.3337"
                stroke="white"
                stroke-width="1.25"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
              <path
                d="M6.66699 11.3335H10.0003"
                stroke="white"
                stroke-width="1.25"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
              <path
                d="M10.834 2.58354V3.0002C10.834 5.35723 10.834 6.53574 11.5662 7.26797C12.2985 8.0002 13.477 8.0002 15.834 8.0002H16.2507M16.6673 9.38095V12.1669C16.6673 15.3095 16.6673 16.881 15.691 17.8572C14.7147 18.8335 13.1433 18.8335 10.0007 18.8335C6.85795 18.8335 5.28661 18.8335 4.31029 17.8572C3.33398 16.881 3.33398 15.3095 3.33398 12.1669V8.38007C3.33398 5.67589 3.33398 4.3238 4.07238 3.40798C4.22155 3.22296 4.39008 3.05444 4.57509 2.90526C5.49091 2.16687 6.843 2.16687 9.54715 2.16687C10.1352 2.16687 10.4291 2.16687 10.6983 2.26188C10.7543 2.28164 10.8092 2.30437 10.8627 2.33C11.1203 2.45316 11.3282 2.66104 11.7439 3.07677L15.691 7.0239C16.1727 7.50561 16.4136 7.74647 16.5405 8.05275C16.6673 8.35904 16.6673 8.69966 16.6673 9.38095Z"
                stroke="white"
                stroke-width="1.25"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>

            <button class="text-white px-4 py-2 rounded outline-none">
              Print
            </button>
          </div>
        </div>
      </div>

      <div class="flex flex-col sm:flex-row gap-4 sm:gap-5 text-center mt-4">
        <div class="text-[#0F75BC] text-sm sm:text-base">
          2080-06-10 (04:14 PM)
        </div>
        <div class="flex gap-[10px]">
          <div
            class="bg-[#F5D5D7] w-full sm:w-[96px] h-[31px] mx-auto sm:mx-0 flex items-center justify-center rounded"
          >
            <span
              class="text-[#E00A0A] text-sm sm:text-[14px] font-sans font-medium"
            >
              Emergency
            </span>
          </div>
          <div
            class="bg-[#FFECDC] w-full sm:w-[96px] h-[31px] mx-auto sm:mx-0 flex items-center justify-center rounded"
          >
            <span
              class="text-[#FD7E14] text-sm sm:text-[14px] font-sans font-medium"
            >
              Processing
            </span>
          </div>
        </div>
      </div>
      <div class="flex gap-[15px]">
        <div
          class="bg-[#ffffff] w-[300px] h-[34px] rounded-[2px] mt-[15px] gap-[10px] items-center justify-center flex"
        >
          <div class="font-medium font-sans">Ticket.no</div>
          <div class="text-[#0F75BC] font-sans font-bold text-[16px]">
            HS - 16592 -52464
          </div>
        </div>
        <div
          class="bg-[#ffffff] w-[239px] h-[34px] rounded-[2px] mt-[15px] gap-[10px] items-center justify-center flex"
        >
          <div class="font-medium font-sans">Feedback Scource</div>
          <div class="text-[#0F75BC] font-sans font-bold text-[16px]">
            Twitter
          </div>
        </div>
      </div>
      <div>
        <p
          class="font-sans font-normal mt-4"
          :class="{ 'line-clamp-3': !isExpanded }"
        >
          Whenever my flight is delayed, I find myself questioning the wisdom
          behind purchasing that ticket in the first place. Arriving at Hong
          Kong airport inevitably leads to yet another hotel stay, which is
          becoming all too familiar. This persistent issue with the airline's
          management has prompted me to seriously reconsider my choice to fly
          with Nepal Airlines in the future. The frustration of dealing with
          delays and the inconvenience of unexpected accommodations is starting
          to outweigh the benefits of flying with them.
        </p>

        <button
          @click="toggleView"
          class="text-[#0F75BC] block sm:hidden font-medium mt-2"
        >
          {{ isExpanded ? "View Less" : "View More" }}
        </button>
      </div>
      <div class="mt-[40px]">
        <TextFill />
      </div>
      <div class="mt-[40px]">
        <StatusPage />
      </div>
      <div class="mt-[40px]">
        <OtherComplaints />
      </div>
    </div>
  </div>
</template>
<script setup>
import OtherComplaints from "./OtherComplaints.vue";
import StatusPage from "./StatusPage.vue";
import TextFill from "./TextFill.vue";
import { ref } from "vue";

const isExpanded = ref(false);

const toggleView = () => {
  isExpanded.value = !isExpanded.value;
};
</script>
