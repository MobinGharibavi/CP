<template>
  <div>
    <!-- Modal start -->
    <UtilComponentModal
      title="ساخت درگاه پرداخت (مشخص کنید درگاه پرداخت زیر مجموعه کدام کمپانی باشد)"
      @close="toogleModal"
      :modalActive="modalActive"
    >
      <div class="flex gap-5 px-5 py-2.5 flex-col">
        <div class="flex flex-col gap-2">
          <label for="company">کمپانی</label>
          <select class="input-select" name="company" id="company">
            <option value="test">تست</option>
          </select>
        </div>

        <div class="flex items-center justify-end gap-3">
          <button @click="toogleModal" class="btn-outline">انصراف</button>
          <button class="btn-primary">ادامه ساخت درگاه پرداخت</button>
        </div>
      </div>
    </UtilComponentModal>
    <!-- Modal end -->
    
    <LayoutTopAnyPage title="درگاه پرداخت">
      <button
        @click="toogleModal"
        class="border rounded-lg px-4 py-[0.625rem] flex gap-2 items-center"
      >
        <img src="/icon/add.svg" alt="" />
        <span> ساخت درگاه پرداخت </span>
      </button>
    </LayoutTopAnyPage>
    <PaymentTable title="درگاه پرداخت" />
  </div>
</template>

<script setup>
const modalActive = ref(false);
const toogleModal = () => {
  modalActive.value = !modalActive.value;
  document.querySelector("body").classList.add("overflow-hidden");
};
</script>
