<template>
  <!-- Modal start -->
  <UtilComponentModal
    size="xs"
    :boldTitle="true"
    title="آیا میخواهید سایت ساخته شود؟"
    @close="toogleModal"
    :modalActive="modalActive"
  >
    <p class="text-sm px-5 pb-5">
      بعد از ساخت سایت میتوانید آن را ویرایش و حذف کنید.
    </p>
    <div class="px-5 py-2.5">
      <div class="flex items-center justify-end gap-3">
        <button @click="toogleModal" class="btn-outline">انصراف</button>
        <button class="btn-primary">ساخت سایت</button>
      </div>
    </div>
  </UtilComponentModal>
  <!-- Modal end -->
  <UtilComponentCreatePage title="ساخت سایت">
    <div class="flex flex-col gap-2">
      <div class="grid gap-2 grid-cols-3">
        <div class="flex flex-col w-full gap-2">
          <label for="company">نوع </label>
          <select
            class="input-select"
            placeholder="متن ورودی"
            name="company"
            id="company"
          >
            <option value="test">سایت پرواز</option>
          </select>
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="company">درخواست کننده</label>
          <select
            class="input-select"
            placeholder="متن ورودی"
            name="company"
            id="company"
          >
            <option value="test">آژانس</option>
          </select>
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="company">ملیت</label>
          <select
            class="input-select"
            placeholder="متن ورودی"
            name="company"
            id="company"
          >
            <option value="test">ایران</option>
          </select>
        </div>
      </div>
      <h2 class="font-semibold">عمومی</h2>

      <div class="grid gap-2 grid-cols-2">
        <div class="flex flex-col w-full gap-2">
          <label for="username">سایت</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="username">دامنه سایت</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
      </div>
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
      </div>

      <div class="flex justify-between">
        <h2 class="font-semibold mt-5">تامین کننده</h2>

        <button
          @click="addSupplier"
          class="btn-outline gap-2 flex items-center"
        >
          <img src="/icon/add-b.svg" alt="" />
          <span>تامین کننده جدید</span>
        </button>
      </div>
      <template v-for="(item, index) in suppliers" :key="index">
        <div class="flex items-center w-full gap-2">
          <div class="flex flex-col w-full gap-2">
            <label for="username">تامین کننده</label>
            <input
              v-model="item.name"
              type="text"
              id="username"
              class="border rounded !px-3.5 !py-3"
              placeholder="متن ورودی"
            />
          </div>
          <div class="flex flex-col w-full gap-2">
            <label for="username">سود تامین کننده به درصد</label>

            <div
              class="flex border rounded justify-between px-3.5 py-3 items-center"
            >
              <input
                type="text"
                v-model="item.percentage"
                id="username"
                class="outline-none w-full"
                placeholder="متن ورودی"
              />
              <span>%</span>
            </div>
          </div>
          <div class="flex flex-col w-full gap-2">
            <label for="username">سود تامین کننده به مقدار</label>

            <div
              class="flex border rounded justify-between px-3.5 py-3 items-center"
            >
              <input
                type="text"
                v-model="item.value"
                id="username"
                class="outline-none w-full"
                placeholder="متن ورودی"
              />
              <span>ریال</span>
            </div>
          </div>

          <button @click="deleteSupplier" class="pt-6 px-6">
            <img src="/icon/close.svg" class="h-full w-12" alt="..." />
          </button>
        </div>
      </template>

      <div class="flex mt-5 justify-between">
        <h2 class="font-semibold mt-5">درگاه پرداخت</h2>

        <button class="btn-outline gap-2 flex items-center">
          <img src="/icon/add-b.svg" alt="" />
          <span>درگاه پرداخت جدید</span>
        </button>
      </div>
      <div class="flex items-center w-full gap-2">
        <div class="flex flex-col w-full gap-2">
          <label for="username">درگاه پرداخت</label>
          <input
            type="text"
            id="username"
            class="border rounded !px-3.5 !py-3"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="username">سود درگاه به درصد</label>

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
          <label for="username">سود درگاه به مقدار</label>

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

        <button class="pt-6 px-6">
          <img src="/icon/close.svg" class="h-full w-12" alt="..." />
        </button>
      </div>

      <h2 class="font-semibold mt-5">نرخ مصوب</h2>
      <div class="flex items-center">
        <label class="inline-flex items-center cursor-pointer">
          <input type="checkbox" value="" class="sr-only peer" />
          <div
            class="relative w-11 h-6 bg-gray-200 rounded-full peer peer-focus:ring-4 peer-focus:ring-blue-300 dark:peer-focus:ring-blue-800 dark:bg-gray-700 peer-checked:after:translate-x-full rtl:peer-checked:after:-translate-x-full peer-checked:after:border-white peer-checked:after:content-['\2713'] after:content-[''] after:text-xs after:flex after:justify-center after:items-center after:absolute after:top-0.5 after:start-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all dark:border-gray-600 peer-checked:bg-blue-600"
          ></div>
          <span class="ms-3 text-[#605D64]">
            آیا قیمت های بالاتر از نرخ مصوب برای این سایت نمایش داده شود؟
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

      <h2 class="font-semibold mt-5">رنگ اصلی (کد hex رنگ را وارد کنید)</h2>
      <div class="grid grid-cols-5 gap-2">
        <div class="flex flex-col w-full gap-2">
          <label for="username">رنگ اصلی</label>
          <div class="input-color">
            <input
              v-model="firstColorMain"
              type="color"
              class="w-6 h-6"
              name=""
              id=""
            />
            <span>{{ firstColorMain }}</span>
          </div>
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="username">رنگ اصلی - تینت 1</label>
          <div class="input-color">
            <input type="color" class="w-6 h-6" name="" id="" />
            <span>000#</span>
          </div>
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="username">رنگ اصلی - تینت 2</label>
          <div class="input-color">
            <input type="color" class="w-6 h-6" name="" id="" />
            <span>000#</span>
          </div>
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="username">رنگ اصلی - شید 1</label>
          <div class="input-color">
            <input type="color" class="w-6 h-6" name="" id="" />
            <span>000#</span>
          </div>
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="username">رنگ اصلی - شید 2</label>
          <div class="input-color">
            <input type="color" class="w-6 h-6" name="" id="" />
            <span>000#</span>
          </div>
        </div>
      </div>

      <h2 class="font-semibold mt-5">رنگ ثانویه (کد hex رنگ را وارد کنید)</h2>
      <div class="grid grid-cols-5 gap-2">
        <div class="flex flex-col w-full gap-2">
          <label for="username">رنگ اصلی</label>
          <div class="input-color">
            <input type="color" class="w-6 h-6" name="" id="" />
            <span>000#</span>
          </div>
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="username">رنگ اصلی - تینت 1</label>
          <div class="input-color">
            <input type="color" class="w-6 h-6" name="" id="" />
            <span>000#</span>
          </div>
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="username">رنگ اصلی - تینت 2</label>
          <div class="input-color">
            <input type="color" class="w-6 h-6" name="" id="" />
            <span>000#</span>
          </div>
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="username">رنگ اصلی - شید 1</label>
          <div class="input-color">
            <input type="color" class="w-6 h-6" name="" id="" />
            <span>000#</span>
          </div>
        </div>
        <div class="flex flex-col w-full gap-2">
          <label for="username">رنگ اصلی - شید 2</label>
          <div class="input-color">
            <input type="color" class="w-6 h-6" name="" id="" />
            <span>000#</span>
          </div>
        </div>
      </div>

      <div class="flex mt-5 items-center gap-6">
        <h2 class="font-semibold">فونت</h2>

        <div class="flex gap-2 items-center">
          <input type="checkbox" class="w-4 h-4" name="font" id="font" />
          <label for="font">استفاده از فونت پیشفرض</label>
        </div>
      </div>
      <div class="grid grid-cols-4 gap-2">
        <div class="flex flex-col text-sm text-[#605D64] w-full gap-2">
          <label for="username">فونت - Thin</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col text-sm text-[#605D64] w-full gap-2">
          <label for="username">فونت - Regular</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col text-sm text-[#605D64] w-full gap-2">
          <label for="username">فونت - Bold</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col text-sm text-[#605D64] w-full gap-2">
          <label for="username">فونت - Black</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
      </div>

      <h2 class="font-semibold">نمایش اسم</h2>

      <div class="grid grid-cols-3 gap-2">
        <div class="flex flex-col text-sm text-[#605D64] w-full gap-2">
          <label for="username">اسم - فارسی</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col text-sm text-[#605D64] w-full gap-2">
          <label for="username">اسم - انگلیسی</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col text-sm text-[#605D64] w-full gap-2">
          <label for="username">اسم - عربی</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
      </div>
      <h2 class="font-semibold">نمایش اطلاعات تماس</h2>

      <div class="grid grid-cols-4 gap-2">
        <div class="flex flex-col text-sm text-[#605D64] w-full gap-2">
          <label for="username">ایمیل</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col text-sm text-[#605D64] w-full gap-2">
          <label for="username">شماره تماس - فارسی</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col text-sm text-[#605D64] w-full gap-2">
          <label for="username">شماره تماس - انگلیسی</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col text-sm text-[#605D64] w-full gap-2">
          <label for="username">شماره تماس - عربی</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
        <div class="flex flex-col text-sm text-[#605D64] w-full gap-2">
          <label for="username">آدرس</label>
          <input
            type="text"
            id="username"
            class="input-style"
            placeholder="متن ورودی"
          />
        </div>
      </div>

      <div class="flex items-center justify-end gap-3 mt-10">
        <button class="btn-outline">انصراف</button>
        <button @click="toogleModal" class="btn-primary">ساخت سایت</button>
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
