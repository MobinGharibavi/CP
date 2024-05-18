<template>
  <!-- Modal start -->
  <UtilComponentModal
    size="xs"
    :boldTitle="true"
    title="آیا میخواهید یوزر ساخته شود؟"
    @close="toogleModal"
    :modalActive="modalActive"
  >
    <p class="text-sm px-5 pb-5">
      بعد از ساخت یوزر میتوانید آن را ویرایش و حذف کنید.
    </p>
    <div class="px-5 py-2.5">
      <div class="flex items-center justify-end gap-3">
        <button @click="toogleModal" class="btn-outline">انصراف</button>
        <button class="btn-primary">ساخت یوزر</button>
      </div>
    </div>
  </UtilComponentModal>
  <!-- Modal end -->
  <UtilComponentCreatePage title="ساخت یوزر">
    <div class="flex flex-col gap-2">
      <div class="flex flex-col w-full gap-2">
        <label for="company">نوع یوزر</label>
        <select
          class="input-select"
          placeholder="متن ورودی"
          name="company"
          id="company"
        >
          <option value="test">کانتر من</option>
        </select>
      </div>
      <h2 class="font-semibold">عمومی</h2>

      <div class="grid grid-cols-4 w-full gap-2">
        <div class="flex flex-col w-full gap-2">
          <label for="username">نام و نام خانوادگی</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="username">نام کاربری</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="password">رمز عبور</label>
          <input
            type="password"
            id="password"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="office">شماره تلفن</label>
          <input
            type="text"
            id="office"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="office">ایمیل</label>
          <input
            type="text"
            id="office"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="office">شهر</label>
          <input
            type="text"
            id="office"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="office">نام آژانس</label>
          <input
            type="text"
            id="office"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="office">موقعیت شغلی</label>
          <input
            type="text"
            id="office"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="office">مدیر آژانس</label>
          <input
            type="text"
            id="office"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="office">موبایل مدیر</label>
          <input
            type="text"
            id="office"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="office">تلفن آژانس</label>
          <input
            type="text"
            id="office"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="office">فکس آژانس</label>
          <input
            type="text"
            id="office"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="office">کد امنیتی</label>
          <input
            type="text"
            id="office"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
      </div>

      <h2 class="font-semibold mt-5">کمیسیون</h2>
      <div class="flex items-center w-full gap-2">
        <div class="flex flex-col w-full gap-2">
          <label for="username">کمیسیون به درصد</label>

          <div
            class="flex border rounded justify-between px-3.5 py-3 items-center"
          >
            <input
              type="text"
              id="username"
              class="outline-none w-full"
              placeholder="متن ورودی"
            />
            <span>%</span>
          </div>
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="username">کمیسیون به مقدار</label>

          <div
            class="flex border rounded justify-between px-3.5 py-3 items-center"
          >
            <input
              type="text"
              id="username"
              class="outline-none w-full"
              placeholder="متن ورودی"
            />
            <span>ریال</span>
          </div>
        </div>
      </div>

      <h2 class="font-semibold mt-5">نرخ مصوب</h2>
      <div class="flex items-center">
        <label class="inline-flex items-center cursor-pointer">
          <input type="checkbox" value="" class="sr-only peer" />
          <div
            class="relative w-11 h-6 bg-gray-200 rounded-full peer peer-focus:ring-4 peer-focus:ring-blue-300 dark:peer-focus:ring-blue-800 dark:bg-gray-700 peer-checked:after:translate-x-full rtl:peer-checked:after:-translate-x-full peer-checked:after:border-white peer-checked:after:content-['\2713'] after:content-[''] after:text-xs after:flex after:justify-center after:items-center after:absolute after:top-0.5 after:start-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all dark:border-gray-600 peer-checked:bg-blue-600"
          ></div>
          <span class="ms-3 text-[#605D64]">
            آیا قیمت های بالاتر از نرخ مصوب برای این یوزر نمایش داده شود؟
          </span>
        </label>
      </div>

      <h2 class="font-semibold mt-5">دسترسی ها</h2>
      <div class="grid grid-cols-2 gap-4">
        <div v-for="(item, index) in 4" :key="index" class="flex items-center">
          <label class="inline-flex items-center cursor-pointer">
            <input type="checkbox" value="" class="sr-only peer" />
            <div
              class="relative w-11 h-6 bg-gray-200 rounded-full peer peer-focus:ring-4 peer-focus:ring-blue-300 dark:peer-focus:ring-blue-800 dark:bg-gray-700 peer-checked:after:translate-x-full rtl:peer-checked:after:-translate-x-full peer-checked:after:border-white peer-checked:after:content-['\2713'] after:content-[''] after:text-xs after:flex after:justify-center after:items-center after:absolute after:top-0.5 after:start-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all dark:border-gray-600 peer-checked:bg-blue-600"
            ></div>
            <span class="ms-3 text-[#605D64]"> عنوان دسترسی </span>
          </label>
        </div>
      </div>

      <div class="flex items-center justify-end gap-3 mt-10">
        <button class="btn-outline">انصراف</button>
        <button @click="toogleModal" class="btn-primary">ساخت یوزر</button>
      </div>
    </div>
  </UtilComponentCreatePage>
</template>

<script setup>
const modalActive = ref(false);
const toogleModal = () => {
  modalActive.value = !modalActive.value;
  document.querySelector("body").classList.add("overflow-hidden");
};
</script>
