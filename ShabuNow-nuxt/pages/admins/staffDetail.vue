<template>
  <MainContainer>
    <HeaderContainer>
      <HeaderText>ข้อมูลเจ้าหน้าที่</HeaderText>
    </HeaderContainer>
    <hr />

    <!-- เปลี่ยนรหัสผ่าน -->

    <section class="bg-gray-50 min-h-screen flex items-center justify-center">
      <!-- login container -->
      <div class="bg-gray-100 flex rounded-2xl shadow-lg max-w-3xl p-5">
        <!-- form -->
        <div class="sm:w-1/2 px-8">
          <h1 class="font-bold text-2xl">แก้ไขข้อมูลเจ้าหน้าที่</h1>
          <form action="" class="flex flex-col gap-4">
            <!-- <button class="bg-red-500 text-white rounded-xl ">Log in</button> -->
            <input
              class="p-2 mt-8 rounded-xl border"
              type="text"
              name="firstname"
              placeholder="Firstname"
            />
            <input
              class="p-2 rounded-xl border"
              type="text"
              name="lastname"
              placeholder="Lastname"
            />
            <input
              class="p-2 rounded-xl border"
              type="email"
              name="email"
              placeholder="Email"
            />
            <input
              class="p-2 rounded-xl border"
              type="password"
              name="password"
              placeholder="Password"
            />
            <input
              class="p-2 rounded-xl border"
              type="password"
              name="confirm-password"
              placeholder="Confirm password"
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
            <Button>
              <slot name="button">ยืนยันแก้ไขข้อมูล</slot>
            </Button>
            <br />
          </form>
        </div>
        <!-- image -->
        <div class="w-1/2 sm:block hidden">
          <img
            class="rounded-2xl"
            src="https://images.unsplash.com/photo-1493552152660-f915ab47ae9d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2574&q=80"
            alt=""
          />
        </div>
      </div>
    </section>
  </MainContainer>
</template>
