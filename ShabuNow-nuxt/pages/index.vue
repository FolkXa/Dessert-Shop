<template>
    <MainContainer>
        <HeaderContainer>
            <HeaderText>
                โปรดเลือกเมนูสุดคุ้ม
            </HeaderText>
            <!-- category dropdown button -->
            <ButtonDropdown title="เลือกหมวดหมู่อาหาร" :items="categories" class="mb-4"/>
            <!-- end -->
        </HeaderContainer>
        <hr>
        
        <ContentContainer>
            <!-- menu container -->
            <!-- Category Tag -->
            <HeaderContainer class="w-full">
                <div class="text-2xl font-medium m-4 py-1.5 px-4 rounded-lg bg-red-600 text-white">
                    <h1>ประเภท : อาหารคาว</h1> 
                </div>

                <!-- admin functions -->
                <div class="flex flex-col md:flex-row">
                    <!-- add menu -->
                    <a href="/admins/createMenu"
                    class="text-xl ease-out duration-150 border-black hover:border-red-600 border-2 hover:border-2 hover:text-red-600 cursor-pointer rounded px-1.5 py-1 m-2">
                    <i class="bi bi-plus"></i>
                    เพิ่มเมนู
                    </a>

                    <!-- add category  -->
                    <a href="/admins/addCategory"
                    class="text-xl ease-out duration-150 border-black hover:border-red-600 border-2 hover:border-2 hover:text-red-600 cursor-pointer rounded px-1.5 py-1 m-2">
                    <i class="bi bi-plus"></i>
                    เพิ่มหมวดหมู่
                    </a>
                </div>

            </HeaderContainer>
            <GridContainer>
                <!-- menu item card -->
                <MenuItemCard v-for="food in foods" :imageUrl="food.imageUrl" :add_to_cart="food.link" :edit_menu="food.edit_menu">

                    <template v-slot:title>
                        <!-- สลัดผักรวมมิตร -->
                        {{ food.title }}
                    </template>
                    <template v-slot:price>
                        <!-- ราคา ฿55 บาท -->
                        {{ food.price }}
                    </template>
                    <template v-slot:button>
                        เลือกเมนูนี้
                    </template>
                </MenuItemCard>
                <!-- end -->
            </GridContainer>
            <!-- end menu container -->
        </ContentContainer>
    </MainContainer>
</template>

<script>
export default {
    // just some data
    data() {
        return {
            foods: [
                {
                    imageUrl: 'https://img.freepik.com/free-photo/delicious-vietnamese-food-including-pho-ga-noodles-spring-rolls-white-wall_181624-34158.jpg?w=1480&t=st=1694914784~exp=1694915384~hmac=28ce6696273496ac0f862aacccb0f3fcf9bb4b466ea118dc34c9bc3aaac883b0',
                    title: 'Salad',
                    price: '75',
                    link: 'menus/menu_1',
                    edit_menu: '/admins/editMenu'
                },
                {
                    imageUrl: 'https://img.freepik.com/free-photo/fried-pork-with-garlic-pepper-served-with-rice-fried-egg_1150-27374.jpg?w=1480&t=st=1694917028~exp=1694917628~hmac=817a4137204b388d2caebdb1832e665b25d9137da1a062d8ac87461377696e95',
                    title: 'Fried Pork Rice',
                    price: '85',
                    link: 'menus/menu_2',
                    edit_menu: '/admins/editMenu'
                },
                {
                    imageUrl: 'https://img.freepik.com/free-photo/fried-chicken-parts-fusilli-white-plate_114579-72409.jpg?w=1480&t=st=1694919254~exp=1694919854~hmac=42c4ec7371dcd64d7efcd793238b259b333273cb049d67c36d4a4b26a29294a7',
                    title: 'Pasta and Chicken',
                    price: '125',
                    link: 'menus/menu_3',
                    edit_menu: '/admins/editMenu'
                },
                {
                    imageUrl: 'https://img.freepik.com/free-photo/stir-fried-instant-noodles-with-seafood-variety-vegetable_1150-27317.jpg?w=740&t=st=1694933851~exp=1694934451~hmac=a4574fd32652c87e0203d95bf152a23675fcca588220cc5edd22b30321a3eef4',
                    title: 'Spaghetti',
                    price: '145',
                    link: 'menus/menu_4',
                    edit_menu: '/admins/editMenu'
                }
            ],
            // dropdown button
            categories: [
                {
                    title: 'Food',
                    link: '#'
                },
                {
                    title: 'Drink',
                    link: '#'
                },
                {
                    title: 'Ice Cream',
                    link: '#'
                },
                {
                    title: 'Hot',
                    link: '#'
                }
            ]
        }
    }
}
</script>