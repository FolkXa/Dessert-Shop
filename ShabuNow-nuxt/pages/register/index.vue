<template>
  <section class="bg-gray-50 min-h-screen flex items-center justify-center">
    <!-- login container -->
    <div class="bg-gray-100 flex rounded-2xl shadow-lg max-w-3xl p-5">
      <!-- form -->
      <div class="sm:w-1/2 px-8">
        <h1 class="font-bold text-2xl">Register</h1>
        <p class="mt-4 text-sm">Let's create your account.</p>
        <form action="" class="flex flex-col gap-4 mt-4">
          <InputField
            class=""
            type="text"
            name="firstname"
            placeholder="FirstName"
          />
          <InputField
            class=""
            type="text"
            name="lastname"
            placeholder="LastName"
          />
          <InputField
            class=""
            type="email"
            name="email"
            placeholder="Email"
          />
          <InputField
            class=""
            type="password"
            name="password"
            placeholder="Password"
          />
          <InputField
            class=""
            type="password"
            name="confirm-password"
            placeholder="Confirm Password"
          />
          <div class="mx-auto mt-2">
            <label
              for="example1"
              class="mb-1 block text-sm font-medium text-gray-700"
              >อัพโหลดรูปภาพ</label
            >
            <input
              id="example1"
              type="file"
              class="mt-2 block w-full text-sm file:mr-4 file:rounded-md file:border-0 file:bg-slate-700 file:py-2 file:px-4 file:text-sm file:font-semibold file:text-white hover:file:bg-slate-900 focus:outline-none disabled:pointer-events-none disabled:opacity-60"
            />
          </div>
          <!-- Register Button -->
          <Button>
            <slot name="button"> สมัครสมาชิก </slot>
          </Button>
          <br />
          <!-- Login Here -->
          <p>
            สมัครบัญชีไว้แล้ว?
            <a href="/login" class="underline">เข้าสู่ระบบที่นี่</a>
          </p>
        </form>
        <div class="mt-8 text-red-600 hover:text-red-500 hover:underline">
          <a href="/login">
            <i class="bi bi-arrow-left-short"></i>
            Back To Login
          </a>
        </div>
      </div>
      <!-- image -->
      <div class="w-1/2 sm:block hidden">
        <img
          class="rounded-2xl"
          src="https://images.unsplash.com/photo-1549048085-bab2f1f49f65?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2487&q=80"
          alt=""
        />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
// import { InputField } from '#build/components';

definePageMeta({
  layout: "no-navbar",
});
</script>
