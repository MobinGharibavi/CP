<template>
  <div>
    <main class="flex flex-col bg-white">
      <div class="h-[7.75rem] items-center flex px-8 border-b">
        <div class="flex justify-between w-full">
          <div class="flex flex-col gap-4">
            <div class="flex items-center gap-4">
              <h2 class="text-[1.75rem] font-bold">CrsTrip کمپانی</h2>

              <h6 class="rounded-full py-1 px-4 bg-[#E0DAFF] text-[#5539FF]">
                Company
              </h6>
            </div>

            <span class="text-[#938F96]">ID:12549876532</span>
          </div>

          <div class="flex items-start gap-2">
            <button
              class="border rounded-lg px-4 py-[0.625rem] flex gap-2 items-center"
            >
              <img src="/icon/trash.svg" alt="" />
              <span> حذف </span>
            </button>
            <button
              class="border rounded-lg px-4 py-[0.625rem] flex gap-2 items-center"
            >
              <img src="/icon/edit.svg" alt="" />
              <span> ویرایش </span>
            </button>
          </div>
        </div>
      </div>

      <div class="flex items-center border-b py-2 px-6 gap-8 h-[3.5rem]">
        <div @click="step = 1" :class="{ active: step == 1 }" class="flex cursor-pointer relative py-4 gap-2">
          <svg :class="{ 'active': step == 1 }" class="fill-[#605D64]" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M17.1897 4.96C17.1897 4.97 17.1897 4.97 17.1897 4.98C16.9397 4.97 16.6897 4.96 16.4197 4.96H8.71973L9.78973 3.9C10.7697 2.91 11.8497 2 13.0997 2C14.3597 2 15.4397 2.91 16.4197 3.9L16.9797 4.46C17.1197 4.59 17.1897 4.77 17.1897 4.96Z" />
<path d="M20.84 13.1702C21.23 13.1702 21.54 12.8502 21.54 12.4502V11.5702C21.54 7.6402 20.34 6.4502 16.42 6.4502H10.12H7.57996C3.65996 6.4502 2.45996 7.6502 2.45996 11.5702V12.0002C2.45996 12.4002 2.76996 12.7102 3.15996 12.7102C3.99996 12.7102 4.66996 13.3902 4.66996 14.2202C4.66996 15.0502 3.99996 15.7402 3.15996 15.7402C2.76996 15.7402 2.45996 16.0502 2.45996 16.4502V16.8802C2.45996 20.8102 3.65996 22.0002 7.57996 22.0002H10.11H16.41C20.33 22.0002 21.53 20.8002 21.53 16.8802C21.53 16.4902 21.22 16.1702 20.83 16.1702C19.99 16.1702 19.32 15.5002 19.32 14.6702C19.33 13.8402 20 13.1702 20.84 13.1702ZM10.82 18.8602C10.82 19.2502 10.5 19.5702 10.11 19.5702C9.71996 19.5702 9.39996 19.2502 9.39996 18.8602V16.1802C9.39996 15.7902 9.71996 15.4702 10.11 15.4702C10.5 15.4702 10.82 15.7902 10.82 16.1802V18.8602ZM10.82 12.2702C10.82 12.6602 10.5 12.9802 10.11 12.9802C9.71996 12.9802 9.39996 12.6602 9.39996 12.2702V9.5902C9.39996 9.2002 9.71996 8.8802 10.11 8.8802C10.5 8.8802 10.82 9.2002 10.82 9.5902V12.2702Z" />
</svg>


          <span> بلیط ها </span>
        </div>
        <div @click="step = 2" :class="{ active: step == 2 }" class="flex cursor-pointer relative py-4 gap-2">
          <!-- <img src="/icon/receipt.svg" alt="" /> -->
          <svg :class="{ '!stroke-[#0a77ff]': step == 2 }" class="stroke-[#605D64]" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M6.73 19.7C7.55 18.82 8.8 18.89 9.52 19.85L10.53 21.2C11.34 22.27 12.65 22.27 13.46 21.2L14.47 19.85C15.19 18.89 16.44 18.82 17.26 19.7C19.04 21.6 20.49 20.97 20.49 18.31V7.04C20.5 3.01 19.56 2 15.78 2H8.22C4.44 2 3.5 3.01 3.5 7.04V18.3C3.5 20.97 4.96 21.59 6.73 19.7Z" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M8.09607 11H8.10505" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M10.8984 11H16.3984"  stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M8.09607 7H8.10505"  stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M10.8984 7H16.3984"  stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
</svg>


          <span> تراکنش ها </span>
        </div>
        <div @click="step = 3" :class="{ active: step == 3 }" class="flex cursor-pointer relative py-4 gap-2">
          <!-- <img src="/icon/receipt.svg" alt="" /> -->
          <svg :class="{ 'active': step == 3 }" class="fill-[#605D64]" width="18" height="22" viewBox="0 0 18 22" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M16 13V17H14V13H16ZM4 13V17H3C2.45 17 2 16.55 2 16V13H4ZM9 0C4.03 0 0 4.03 0 9V16C0 17.66 1.34 19 3 19H6V11H2V9C2 5.13 5.13 2 9 2C12.87 2 16 5.13 16 9V11H12V19H16V20H9V22H15C16.66 22 18 20.66 18 19V9C18 4.03 13.97 0 9 0Z" />
</svg>


          <span> پشتیبانی ها </span>
        </div>
        <div @click="step = 4" :class="{ '!stroke-[#0a77ff]  active': step == 4 }" class="flex cursor-pointer relative py-4 gap-2">
          <svg class="stroke-[#605D64]" :class="{ 'active !stroke-white': step == 4 }" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<g clip-path="url(#clip0_190_16018)">
<path d="M8 16H5.43C3.14 16 2 14.86 2 12.57V5.43C2 3.14 3.14 2 5.43 2H10C12.29 2 13.43 3.14 13.43 5.43"  stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M18.5701 22H14.0001C11.7101 22 10.5701 20.86 10.5701 18.57V11.43C10.5701 9.14 11.7101 8 14.0001 8H18.5701C20.8601 8 22.0001 9.14 22.0001 11.43V18.57C22.0001 20.86 20.8601 22 18.5701 22Z" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M14.8701 15H18.1301"  stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M16.5 16.6301V13.3701"  stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
</g>
<defs>
<clipPath id="clip0_190_16018">
<rect width="24" height="24" fill="white"/>
</clipPath>
</defs>
</svg>



          <span> سایت ها </span>
        </div>
        <div @click="step = 5" :class="{ active: step == 5 }" class="flex cursor-pointer relative py-4 gap-2">

          <svg :class="{ 'active': step == 5 }" class="fill-[#605D64]"  width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M9.16006 10.87C9.06006 10.86 8.94006 10.86 8.83006 10.87C6.45006 10.79 4.56006 8.84 4.56006 6.44C4.56006 3.99 6.54006 2 9.00006 2C11.4501 2 13.4401 3.99 13.4401 6.44C13.4301 8.84 11.5401 10.79 9.16006 10.87Z" stroke="#605D64" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M16.41 4C18.35 4 19.91 5.57 19.91 7.5C19.91 9.39 18.41 10.93 16.54 11C16.46 10.99 16.37 10.99 16.28 11" stroke="#605D64" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M4.15997 14.56C1.73997 16.18 1.73997 18.82 4.15997 20.43C6.90997 22.27 11.42 22.27 14.17 20.43C16.59 18.81 16.59 16.17 14.17 14.56C11.43 12.73 6.91997 12.73 4.15997 14.56Z" stroke="#605D64" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M18.3401 20C19.0601 19.85 19.7401 19.56 20.3001 19.13C21.8601 17.96 21.8601 16.03 20.3001 14.86C19.7501 14.44 19.0801 14.16 18.3701 14" stroke="#605D64" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
</svg>



          <span> یوزر ها </span>
        </div>

        <div @click="step = 6" :class="{ active: step == 6 }" class="flex cursor-pointer gap-2 relative py-4">
          <!-- <img src="/icon/wallet-search.svg" alt="" /> -->
          <svg class="stroke-[#605D64]" :class="{ 'active !stroke-[#0a77ff] !fill-none': step == 6 }"  width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M12 22H17C20 22 22 20 22 17V12C22 9.3 20.3 7.3 17.8 7C17.6 7 17.3 7 17 7H7C6.7 7 6.5 6.99998 6.2 7.09998C3.6 7.39998 2 9.3 2 12C2 12.3 2 12.7 2 13"  stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M17.8002 6.99922C17.6002 6.99922 17.3002 6.99922 17.0002 6.99922H7.0002C6.7002 6.99922 6.5002 6.99919 6.2002 7.09919C6.3002 6.79919 6.5002 6.59921 6.8002 6.29921L10.0002 2.99922C11.4002 1.59922 13.6002 1.59922 15.0002 2.99922L16.8002 4.79921C17.4002 5.39921 17.7002 6.19922 17.8002 6.99922Z" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M22 12.5H19C17.9 12.5 17 13.4 17 14.5C17 15.6 17.9 16.5 19 16.5H22"  stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M5.80157 21.4C7.57157 21.4 9.00156 19.97 9.00156 18.2C9.00156 16.43 7.57157 15 5.80157 15C4.03157 15 2.60156 16.43 2.60156 18.2C2.60156 19.97 4.03157 21.4 5.80157 21.4Z" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M2 22L3 21"  stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

          <span> حسابداری </span>
          <!-- <img src="/icon/send.svg" alt="" /> -->
          <svg class="stroke-[#605D64]" :class="{ 'active !stroke-[#0a77ff] !fill-none': step == 6 }" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M3.5 22H20.5"  stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M5 3.5L19 17.5"  stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M5 13.77V3.5H15.27" stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

        </div>
      </div>
    </main>

    <CompanyTableTickets v-if="step == 1" title="بلیط ها" />
    <CompanyTableTrans v-if="step == 2" title="تراکنش ها" />
    <CompanyTableSupport v-if="step == 3" title="پشتیبانی" />
    <CompanyTableSites v-if="step == 4" title="سایت ها" />
    <CompanyTableUsers v-if="step == 5" title="یوزر ها" />
  </div>
</template>

<script setup>
const step = ref(1);
</script>
