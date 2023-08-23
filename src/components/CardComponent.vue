<template>
   <div class="card max-w-[150px] p-1 bg-white">
      <p
         class="mb-2 text-md tracking-tight text-gray-900 dark:text-white text-center">
         Noteworthy <slot></slot>
      </p>
   </div>
</template>

<style scoped lang="scss">
.card {
   border-radius: 25px;
   border: 1px solid #ededed;
}
</style>
