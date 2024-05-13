<template>
  <div class="flex font-Kalameh">
    <LayoutSideBar
      :class="{ '-mr-64': !showSidebar }"
      :showHide="sidebarShow"
      class="transition-all duration-500 ease-out"
    />
    <div
      :class="{ 'lg:mr-[16.5rem]': showSidebar }"
      class="flex flex-col min-h-screen w-full transition-all duration-500 ease-out"
    >
      <div
        class="flex shadow items-center sticky top-0 bg-gray-50 z-50 w-full justify-between px-8 h-[4rem]"
      >
        <Icon
          @click="sidebarShow"
          class="cursor-pointer lg:!hidden"
          name="heroicons:bars-3-bottom-right"
          size="30px"
        />

        <div class="flex items-end gap-1">
          <span>...</span>
          /
          <span class="text-[#938F96]">حسابداری</span>
          /
          <span>لیست حساب ها</span>
        </div>

        <div class="flex items-center gap-10">
          <div
            class="bg-[#F7F8F9] rounded w-[19.5rem] h-[2.5rem] flex justify-around items-center"
          >
            <img src="/icon/search-normal.svg" alt="" />
            <input
              type="text"
              class="outline-none bg-transparent"
              placeholder="جستجو در سیستم..."
            />
          </div>

          <div class="flex border rounded-full px-4 py-1 items-center gap-2.5">
            <img src="/icon/Vector.svg" alt="" />
            <span>Hossein Ahmadiyan</span>
            <img src="/icon/user.svg" alt="" />
          </div>
        </div>
      </div>
      <slot />
    </div>
  </div>
</template>

<script lang="ts" setup>
const { isMobile, isTablet } = useDevice();
const showSidebar = ref(isMobile || isTablet ? false : true);

const { width } = useWindowSize();

const route = useRoute();
watch(
  () => route.fullPath,
  () => {
    if (width.value <= 992) {
      showSidebar.value = false;
    }
  },
  {
    immediate: true,
    deep: true,
  }
);

const counselling = ref<object[]>([]);

const showNotif = ref(false);
const clickOutNotif = () => {
  if (showNotif.value) {
    showNotif.value = false;
  }
};

const showMessage = ref(false);
const clickOutMessage = () => {
  if (showMessage.value) {
    showMessage.value = false;
  }
};

function sidebarShow() {
  showSidebar.value = !showSidebar.value;
}
const sppinerLoader = ref(true);
onBeforeMount(() => {
  sppinerLoader.value = true;
});
onMounted(() => {
  sppinerLoader.value = false;
});
</script>
