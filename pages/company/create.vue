<template>
  <!-- Modal start -->
  <UtilComponentModal
    size="xs"
    :boldTitle="true"
    title="آیا میخواهید کمپانی ساخته شود؟"
    @close="toogleModal"
    :modalActive="modalActive"
  >
    <p class="text-sm px-5 pb-5">
      بعد از ساخت کمپانی میتوانید آن را ویرایش و حذف کنید.
    </p>
    <div class="px-5 py-2.5">
      <div class="flex items-center justify-end gap-3">
        <button @click="toogleModal" class="btn-outline">انصراف</button>
        <button class="btn-primary">ساخت کمپانی</button>
      </div>
    </div>
  </UtilComponentModal>
  <!-- Modal end -->
  <UtilComponentCreatePage title="ساخت کمپانی">
    <div class="flex flex-col gap-2">
      <h2 class="font-semibold">عمومی</h2>
      <div class="flex flex-col w-full gap-2">
        <label for="company_name">نام کمپانی </label>
        <input
          type="text"
          id="company_name"
          class="input-style"
          placeholder="متن ورودی"
        />
      </div>

      <h2 class="font-semibold">درخواست کننده</h2>
      <div class="grid grid-cols-4 w-full gap-2">
        <div class="flex flex-col w-full gap-2">
          <label for="username_main">نام و نام خانوادگی</label>
          <input
            type="text"
            id="username_main"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="mobile">شماره همراه</label>
          <input
            type="text"
            id="mobile"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="office">شماره ثابت</label>
          <input
            type="text"
            id="office"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="email">ایمیل</label>
          <input
            type="text"
            id="email"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="name_co">نام شرکت</label>
          <input
            type="text"
            id="name_co"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="address_co">آدرس شرکت</label>
          <input
            type="text"
            id="address_co"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="phone_co">تلفن شرکت</label>
          <input
            type="text"
            id="phone_co"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="email_co">ایمیل شرکت</label>
          <input
            type="text"
            id="email_co"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
      </div>

      <div class="flex items-center justify-end gap-3 mt-10">
        <button class="btn-outline">انصراف</button>
        <button @click="toogleModal" class="btn-primary">ساخت کمپانی</button>
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

const suppliers = ref([
  {
    name: "",
    percentage: "",
    value: "",
  },
]);
const addSupplier = () => {
  suppliers.value.push({
    name: "",
    percentage: "",
    value: "",
  });
};
const deleteSupplier = () => {
  if (suppliers.value.length > 1) {
    suppliers.value.splice(-1, 1);
  }
};

const firstColorMain = ref("#000");
</script>
