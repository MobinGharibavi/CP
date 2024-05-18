<template>
  <div>
    <LayoutTopAnyPage title="کمپانی ها">
      <NuxtLink
        to="/company/create"
        class="border rounded-lg px-4 py-[0.625rem] flex gap-2 items-center"
      >
        <img src="/icon/add.svg" alt="" />
        <span> ساخت کمپانی </span>
      </NuxtLink>
    </LayoutTopAnyPage>
    <CompanyTable title="کمپانی ها" />
  </div>
</template>
