<template>
  <div class="overflow-x-auto px-4 mx-auto mt-5 mb-8">
    <div
      class="flex justify-between rounded-t-lg px-2 py-4 border-t border-x items-center"
    >
      <h6 class="font-semibold">{{ title }}</h6>

      <div class="flex items-center gap-5">
        <div class="flex gap-2 items-center">
          <img src="/icon/search-normal.svg" alt="..." />
          <span>جستجو</span>
        </div>
        <div class="flex gap-2 items-center">
          <img src="/icon/calendar.svg" alt="..." />
          <span>فیلتر تاریخ</span>
        </div>
        <div class="flex gap-2 items-center">
          <img src="/icon/export.svg" alt="..." />
          <span>خروجی</span>
        </div>

        <span>14 سند</span>
      </div>
    </div>
    <table class="table-auto border-collapse rounded-b-lg border w-full">
      <thead class="text-[14px] uppercase">
        <tr>
          <th class="p-2 whitespace-nowrap flex justify-center">
            <div class="text-start">
              <div class="inline-flex items-center">
                <label
                  class="relative flex items-center rounded-full cursor-pointer"
                  htmlFor="checkbox"
                >
                  <!-- before:h-12 before:w-12 -->
                  <input
                    type="checkbox"
                    class="before:content[''] peer relative h-6 w-6 cursor-pointer appearance-none rounded-md border-blue-gray-200 transition-all before:absolute before:top-2/4 before:left-2/4 before:block before:-translate-y-2/4 before:-translate-x-2/4 before:rounded-full bg-[#F0F1F2] before:bg-gray-500 before:opacity-0 before:transition-opacity checked:border-[#0A77FF] checked:bg-[#0A77FF] checked:before:bg-[#0A77FF] hover:before:opacity-10"
                    id="checkbox"
                  />
                  <span
                    class="absolute text-white transition-opacity opacity-0 pointer-events-none top-2/4 left-2/4 -translate-y-2/4 -translate-x-2/4 peer-checked:opacity-100"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      class="h-3.5 w-3.5"
                      viewBox="0 0 20 20"
                      fill="currentColor"
                      stroke="currentColor"
                      stroke-width="1"
                    >
                      <path
                        fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"
                      ></path>
                    </svg>
                  </span>
                </label>
              </div>
            </div>
          </th>
          <th class="p-2 whitespace-nowrap border">
            <div class="text-start">ردیف</div>
          </th>
          <th class="p-2 whitespace-nowrap border">
            <div class="text-start">مسافرین</div>
          </th>
          <th class="p-2 whitespace-nowrap border">
            <div class="text-start">کمپانی</div>
          </th>
          <th class="p-2 whitespace-nowrap border">
            <div class="text-start">سایت</div>
          </th>
          <th class="p-2 whitespace-nowrap border">
            <div class="text-start">تاریخ و ساعت رزرو</div>
          </th>
          <th class="p-2 whitespace-nowrap border">
            <div class="text-start">کد آژانس</div>
          </th>
          <th class="p-2 whitespace-nowrap border">
            <div class="text-start">تامین کننده و رفرنس</div>
          </th>
          <th class="p-2 whitespace-nowrap border">
            <div class="text-start">تیکت ID</div>
          </th>
          <th class="p-2 whitespace-nowrap border">
            <div class="text-start">وضعیت</div>
          </th>
        </tr>
      </thead>
      <tbody class="text-sm">
        <tr
          class="hover:bg-gray-100 text-[#605D64] text-sm transition-all border hover:transition-all"
          v-for="(rowItem, index) in 3 as any"
          :key="index"
        >
          <td class="px-2 flex justify-center py-4 whitespace-nowrap">
            <div class="inline-flex items-center">
              <label
                class="relative flex items-center rounded-full cursor-pointer"
                htmlFor="checkbox"
              >
                <!-- before:h-12 before:w-12 -->
                <input
                  type="checkbox"
                  class="before:content[''] peer relative h-6 w-6 cursor-pointer appearance-none rounded-md border-blue-gray-200 transition-all before:absolute before:top-2/4 before:left-2/4 before:block before:-translate-y-2/4 before:-translate-x-2/4 before:rounded-full bg-[#F0F1F2] before:bg-gray-500 before:opacity-0 before:transition-opacity checked:border-[#0A77FF] checked:bg-[#0A77FF] checked:before:bg-[#0A77FF] hover:before:opacity-10"
                  id="checkbox"
                />
                <span
                  class="absolute text-white transition-opacity opacity-0 pointer-events-none top-2/4 left-2/4 -translate-y-2/4 -translate-x-2/4 peer-checked:opacity-100"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-3.5 w-3.5"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                    stroke="currentColor"
                    stroke-width="1"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                      clip-rule="evenodd"
                    ></path>
                  </svg>
                </span>
              </label>
            </div>
          </td>
          <td class="px-2 border py-4 whitespace-nowrap">{{ index + 1 }}</td>
          <td class="px-2 py-4 flex justify-center whitespace-nowrap">
            <img src="/icon/add.svg" alt="" />
          </td>
          <td
            class="px-2 border py-4 whitespace-nowrap text-[#0A77FF] underline"
          >
            CrsTrip.
          </td>
          <td
            class="px-2 border py-4 whitespace-nowrap text-[#0A77FF] underline"
          >
            crstrip.com
          </td>
          <td class="px-2 border py-4 whitespace-nowrap">20/02/1403 - 22:30</td>
          <td class="px-2 border py-4 whitespace-nowrap">569874516</td>
          <td class="px-2 border py-4 whitespace-nowrap">پرتو - 4565</td>
          <td class="px-2 border py-4 whitespace-nowrap">1359821</td>

          <td class="px-2 bg-[#FFE2E8] border py-4 whitespace-nowrap">
            <div class="flex justify-between">
              <span> خطا </span>

              <img src="/icon/add.svg" alt="" />
            </div>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup lang="ts">
const { row, title } = defineProps<{
  row?: object[];
  title: string;
}>();
</script>
