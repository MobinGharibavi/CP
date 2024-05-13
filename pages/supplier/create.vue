<template>
   <!-- Modal start -->
   <UtilComponentModal
    size="xs"
    :boldTitle="true"
    title="آیا میخواهید تامین کننده ساخته شود؟"
    @close="toogleModal"
    :modalActive="modalActive"
  >
    <p class="text-sm px-5 pb-5">
      بعد از ساخت تامین کننده میتوانید آن را ویرایش و حذف کنید.
    </p>
    <div class="px-5 py-2.5">
      <div class="flex items-center justify-end gap-3">
        <button @click="toogleModal" class="btn-outline">انصراف</button>
        <button class="btn-primary">ساخت تامین کننده</button>
      </div>
    </div>
  </UtilComponentModal>
  <!-- Modal end -->
  <UtilComponentCreatePage title="ساخت تامین کننده">
    <div class="flex flex-col gap-2">
      <h2 class="font-semibold">عمومی</h2>
      <div class="flex items-center w-full gap-2">
        <div class="flex flex-col w-full gap-2">
          <label for="company">تامین کننده</label>
          <select
            class="input-select"
            placeholder="متن ورودی"
            name="company"
            id="company"
          >
            <option value="test">تست</option>
          </select>
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="company">مالک تامین کننده</label>
          <select
            class="input-select"
            placeholder="متن ورودی"
            name="company"
            id="company"
          >
            <option value="test">تست</option>
          </select>
        </div>
      </div>

      <div class="flex items-center w-full gap-2">
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
          <label for="office">Office ID</label>
          <input
            type="text"
            id="office"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
      </div>

      <h2 class="font-semibold mt-5">سود تامین کننده</h2>
      <div class="flex items-center w-full gap-2">
        <div class="flex flex-col w-full gap-2">
          <label for="username">مقدار سود به درصد</label>

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
          <label for="username">مقدار سود به مقدار</label>

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

      <h2 class="font-semibold mt-5">دسترسی</h2>
      <div class="flex items-center">
        <label class="inline-flex items-center cursor-pointer">
          <input type="checkbox" value="" class="sr-only peer" />
          <div
            class="relative w-11 h-6 bg-gray-200 rounded-full peer peer-focus:ring-4 peer-focus:ring-blue-300 dark:peer-focus:ring-blue-800 dark:bg-gray-700 peer-checked:after:translate-x-full rtl:peer-checked:after:-translate-x-full peer-checked:after:border-white peer-checked:after:content-['\2713'] after:content-[''] after:text-xs after:flex after:justify-center after:items-center after:absolute after:top-0.5 after:start-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all dark:border-gray-600 peer-checked:bg-blue-600"
          ></div>
          <span
          class="ms-3 text-[#605D64]"
          >
            تامین کننده برای تمام سیستم در دسترس باشد.
          </span>
        </label>
      </div>

      <div class="flex items-center justify-end gap-3">
        <button class="btn-outline">انصراف</button>
        <button @click="toogleModal" class="btn-primary">ساخت تامین کننده</button>
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