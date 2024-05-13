<template>
  <div
    class="w-[16.5rem] bg-[#1D1B20] border-l shadow-lg lg:shadow-none z-[9999] lg:z-0 h-screen fixed hover:overflow-y-auto overflow-y-hidden"
  >
    <div
      class="relative flex gap-2 justify-center items-center bg-white h-[4rem]"
    >
      <NuxtLink to="/" class="text-[#0A77FF] font-bold text-[2rem]">
        CP
      </NuxtLink>
      <span class="text-[#1D1B20]"> (Control Panel) </span>
      <div
        @click="showHide"
        class="absolute lg:hidden top-5 cursor-pointer left-5"
      >
        <Icon name="ph:x-bold" />
      </div>
    </div>

    <p class="px-5 text-[#938F96] mb-5 mt-6">منو</p>
    <div class="px-5 text-white">
      <ul class="space-y-3">
        <li
          :class="{
            'bg-white/10 text-white': $route.path === item.href,
          }"
          v-for="(item, index) in itemSideBar"
          :key="index"
        >
          <div
            class="flex px-5 py-3 cursor-pointer rounded-md hover:bg-white/10 transition-all hover:transition-all items-center justify-between"
            @click="item.openSubMenu = !item.openSubMenu"
            :class="{
              'bg-white/10 text-white hover:!bg-white/10':
                $route.path === item.href,
            }"
          >
            <div class="flex gap-2 items-center">
              <Icon :name="item.icon" size="1.3rem" />
              <NuxtLink
                v-if="!item.subMenu"
                :target="item.target ? '_blank' : '_self'"
                :to="item.href"
              >
                <span>{{ item.name }}</span>
              </NuxtLink>
              <span v-else>{{ item.name }}</span>
            </div>
            <Icon
              v-if="item.subMenu"
              :rotate="item.openSubMenu ? 2 : 0"
              name="mingcute:down-line"
            />
          </div>
          <TransitionExpand>
            <ul
              v-if="item.openSubMenu"
              :class="{ 'pr-4 space-y-3 pt-3': item.subMenu }"
            >
              <li v-for="(subItem, index) in item.subMenu" :key="index">
                <NuxtLink
                  :to="subItem.href"
                >
                  {{ subItem.title }}
                </NuxtLink>
              </li>
            </ul>
          </TransitionExpand>
        </li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts" setup>
const { showHide }: any = defineProps({
  showHide: Function,
});
interface subMenuItems {
  title: string;
  href: string;
}

interface sideMenu {
  icon: string;
  name: string;
  href?: string;
  subMenu: subMenuItems[] | null;
  openSubMenu?: boolean;
  target?: boolean;
}

const itemSideBar = reactive<sideMenu[]>([
  {
    icon: "ion:grid",
    name: "پرواز",
    subMenu: [
      { title: "بلیط ها", href: "/fly/ticket" },
      { title: "پرواز های دستی", href: "/fly/hand" },
      { title: "ایجاد پرواز", href: "/fly/create" },
    ],
    openSubMenu: false,
    target: false,
  },
  {
    icon: "bi:shop",
    name: "تراکنش ها",
    subMenu: null,
    openSubMenu: false,
    href: "/transaction",
    target: false,
  },
  {
    icon: "eos-icons:products-outlined",
    name: "پشتیبانی",
    subMenu: [{ title: "درباره ما", href: "/product/" }],
    openSubMenu: false,
    target: false,
  },
  {
    icon: "carbon:category-new-each",
    name: "کمپانی ها",
    subMenu: [
      { title: "لیست کمپانی ها", href: "/company/" },
      { title: "ساخت کمپانی جدید", href: "/company/create" },
    ],
    openSubMenu: false,
    target: false,
  },
  {
    icon: "material-symbols:user-attributes",
    name: "سایت ها",
    subMenu: [
      { title: "لیست سایت ها", href: "/sites/" },
      { title: "ساخت سایت جدید", href: "/sites/create" },
    ],
    openSubMenu: false,
    target: false,
  },
  {
    icon: "carbon:partition-specific",
    name: "یوزر ها",
    subMenu: [
      { title: "لیست یوزر ها ", href: "/users/" },
      { title: "ساخت یوزر جدید", href: "/users/create" },
    ],
    openSubMenu: false,
    target: false,
  },
  {
    icon: "bi:tags",
    name: "درگاه پرداخت",
    subMenu: [
      { title: "لیست درگاه های پرداخت", href: "/" },
      { title: "ساخت درگاه پرداخت جدید", href: "/payment/create" },
    ],
    openSubMenu: false,
    target: false,
  },
  {
    icon: "solar:users-group-two-rounded-linear",
    name: "تامین کننده ها",
    subMenu: [
      { title: "لیست تامین کننده ها", href: "/supplier/" },
      { title: "ساخت تامین کننده جدید", href: "/supplier/create" },
    ],
    openSubMenu: false,
    target: false,
  },
]);
</script>
