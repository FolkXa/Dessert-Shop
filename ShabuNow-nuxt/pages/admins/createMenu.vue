<template>
  <MainContainer>
    <HeaderContainer>
      <HeaderText>สร้างเมนู</HeaderText>
    </HeaderContainer>
    <hr />
    <ContentContainer>
      <div class="w-2/3 p-4 text-xl font-light border rounded-xl mt-8 ">

        <div class="overflow-hidden border h-[150px] flex flex-col lg:flex-row justify-around items-center rounded-xl bg-cover-category object-cover bg-center bg-no-repeat">
          <h1 class="text-xl lg:text-3xl font-semibold text-white z-10">
            เพิ่มเมนูอาหาร
          </h1>
          <div class="z-10 text-white text-6xl lg:text-8xl">
            <i class="fa-solid fa-bowl-food"></i>
          </div>
          <div class="bg-cover-overlay"></div>
        </div>

        <InputField
        class="mt-4"
        placeholder="ชื่อเมนู"
        type="text"
        name="confirm-password"
        />
        <InputField
        class="mt-4"
        placeholder="ราคา (THB)"
        type="number"
        name="confirm-password"
        />
        <select
        class="mt-4 text-base text-slate-400 focus:ring-red-600 focus:border-red-600 focus:ring-1 focus:outline-none p-2.5 block bg-white border border-slate-300 rounded-md w-full py-3 pl-9 pr-3"
        >
          <option selected>เลือกหมวดหมู่</option>
          <option value="food">อาหาร</option>
          <option value="drink">เครื่องดื่ม</option>
          <option value="sweet">ของหวาน</option>
        </select>

        <textarea
        row="2"
          class="mt-4 text-base block p-2.5 w-full bg-white border border-slate-300 rounded-lg focus:ring-red-600 focus:border-red-600 focus:ring-1 focus:outline-none"
          placeholder="คำอธิบายเพิ่มเติม"
        ></textarea>

        <div class="mx-auto my-8">
          <label
            class="mt-4 mb-1 block text-lg font-medium text-gray-700"
            >อัพโหลดรูปภาพ</label
          >
          <input
            id="example1"
            type="file"
            class="mt-2 block w-full text-sm file:mr-4 file:rounded-md file:border-0 file:bg-slate-700 file:py-2 file:px-4 file:text-sm file:font-semibold file:text-white hover:file:bg-slate-900 focus:outline-none disabled:pointer-events-none disabled:opacity-60"
          />
        </div>
        <hr class="mt-4">
        <Button class="mt-4 w-full">
          <slot name="button">ยืนยัน</slot>
        </Button>
      </div>
    </ContentContainer>
  </MainContainer>
</template>

<style>
.bg-cover-category {
  position: relative;
  background-image: url('../../assets/img/cover1.jpg');
  background-position: center;
}
.bg-cover-overlay {
  background-color: rgba(0, 0, 0, .35);
  width: 100%;
  height: 100%;
  position: absolute;
}
</style>