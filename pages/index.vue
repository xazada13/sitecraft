<script setup>
useHead({
    link: [
        {
            rel: 'stylesheet',
            href: 'https://fonts.googleapis.com/css2?family=Ballet:opsz@16..72&family=Geologica:wght@100..900&family=Martian+Mono:wght@100..800&family=Montserrat:ital,wght@0,100..900;1,100..900&family=Playfair+Display:ital,wght@0,400..900;1,400..900&family=Raleway:ital,wght@0,100..900;1,100..900&family=Shadows+Into+Light&display=swap'
        }
    ],
    title: 'Тимофей - Commodi numquam sapilki fugit!',
    meta: [
        { name: 'description', content: 'Training site MSHP' },
    ],
})
const menuOpen = ref(false)
</script>
<template>
    <header
        class="flex items-center justify-between md:max-w-6xl w-full lg:mx-auto sticky top-[0px] backdrop-blur-md py-[20px] z-20 md:rounded-b-lg px-[20px]">
        <div class="flex items-center cursor-pointer">
            <div class="flex gap-0 hover:gap-2 mr-[-5px] transition-all duration-150">
                <svg class="mr-[-22px] text-white" xmlns="http://www.w3.org/2000/svg" width="32" height="32"
                    viewBox="0 0 24 24">
                    <g fill="none" fill-rule="evenodd">
                        <path
                            d="M24 0v24H0V0zM12.594 23.258l-.012.002l-.071.035l-.02.004l-.014-.004l-.071-.036q-.016-.004-.024.006l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427q-.004-.016-.016-.018m.264-.113l-.014.002l-.184.093l-.01.01l-.003.011l.018.43l.005.012l.008.008l.201.092q.019.005.029-.008l.004-.014l-.034-.614q-.005-.018-.02-.022m-.715.002a.02.02 0 0 0-.027.006l-.006.014l-.034.614q.001.018.017.024l.015-.002l.201-.093l.01-.008l.003-.011l.018-.43l-.003-.012l-.01-.01z" />
                        <path fill="currentColor"
                            d="M13.707 8.465a1 1 0 0 1 0 1.414L11.586 12l2.121 2.121a1 1 0 0 1-1.414 1.415l-2.828-2.829a1 1 0 0 1 0-1.414l2.828-2.828a1 1 0 0 1 1.414 0" />
                    </g>
                </svg>
                <svg class="text-white" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24">
                    <g fill="none" fill-rule="evenodd">
                        <path
                            d="M24 0v24H0V0zM12.594 23.258l-.012.002l-.071.035l-.02.004l-.014-.004l-.071-.036q-.016-.004-.024.006l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427q-.004-.016-.016-.018m.264-.113l-.014.002l-.184.093l-.01.01l-.003.011l.018.43l.005.012l.008.008l.201.092q.019.005.029-.008l.004-.014l-.034-.614q-.005-.018-.02-.022m-.715.002a.02.02 0 0 0-.027.006l-.006.014l-.034.614q.001.018.017.024l.015-.002l.201-.093l.01-.008l.003-.011l.018-.43l-.003-.012l-.01-.01z" />
                        <path fill="currentColor"
                            d="M10.293 8.465a1 1 0 0 0 0 1.414L12.414 12l-2.121 2.121a1 1 0 0 0 1.414 1.415l2.829-2.829a1 1 0 0 0 0-1.414l-2.829-2.828a1 1 0 0 0-1.414 0" />
                    </g>
                </svg>
            </div>
            <h1 class="text-xl font-semibold text-white">SiteCraft</h1>
        </div>
        <nav class="hidden md:block">
            <ol class="flex items-center gap-16">
                <li class="text-sm text-zinc-200 cursor-pointer hover:mb-1 transition-all duration-150">
                    <NuxtLink to="#info">
                        <p>Обо мне</p>
                    </NuxtLink>
                </li>
                <li class="text-sm text-zinc-200 cursor-pointer hover:mb-1 transition-all duration-150">
                    <NuxtLink to="#stack">
                        <p>Стек</p>
                    </NuxtLink>
                </li>
                <li class="text-sm text-zinc-200 cursor-pointer hover:mb-1 transition-all duration-150">
                    <NuxtLink>
                        <p>Проекты</p>
                    </NuxtLink>
                </li>
                <li class="text-sm text-zinc-200 cursor-pointer hover:mb-1 transition-all duration-150">
                    <NuxtLink to="#contacts">
                        <p>Контакты</p>
                    </NuxtLink>
                </li>
            </ol>
        </nav>
        <button @click="menuOpen = true" class=" md:hidden">
            <svg class="text-white" xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24">
                <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                    stroke-width="1.5" d="M4 5h16M4 12h16M4 19h16" color="currentColor" />
            </svg>
        </button>

    </header>
    <section v-if="menuOpen" @click="menuOpen = false"
        class="fixed top-0 left-0 w-full h-full bg-black/90 z-50 flex flex-col items-center justify-center">
        <nav class="flex flex-col items-center justify-center gap-7">
            <NuxtLink to="#info" class="text-white text-sm">
                <h2>Обо мне</h2>
            </NuxtLink>
            <NuxtLink to="#stack" class="text-white text-sm">
                <h2>Стек</h2>
            </NuxtLink>
            <NuxtLink class="text-white text-sm">
                <h2>Проекты</h2>
            </NuxtLink>
            <NuxtLink to="#contacts" class="text-white text-sm">
                <h2>Контакты</h2>
            </NuxtLink>
        </nav>
    </section>
    <section id="home" class="h-screen max-w-5xl mx-[6%] lg:mx-auto mt-[-70px]">
        <div class="flex items-center justify-center md:justify-between h-screen">
            <div>
                <p class="text-zinc-300 mx-auto w-max md:mx-0 md:text-sm text-xs mb-[20px]">Сайт портфолио
                    web-разработчика
                </p>
                <div
                    class="text-white mx-auto md:mx-0 w-max md:w-min md:text-5xl lg:text-7xl text-4xl font-[800] flex md:flex-col">
                    <div class="flex"><span
                            class="lg:hover:text-[90px] md:hover:text-[70px] transition-all duration-200">
                            <h1>H</h1>
                        </span><span class="lg:hover:text-[90px] md:hover:text-[70px] transition-all duration-200">
                            <h1>e</h1>
                        </span><span class="lg:hover:text-[90px] md:hover:text-[70px] transition-all duration-200">
                            <h1>l</h1>
                        </span><span class="lg:hover:text-[90px] md:hover:text-[70px] transition-all duration-200">
                            <h1>l</h1>
                        </span><span class="lg:hover:text-[90px] md:hover:text-[70px] transition-all duration-200">
                            <h1>o,</h1>
                        </span>
                    </div>
                    <div class="flex">
                        <span class="lg:hover:text-[90px] md:hover:text-[70px] transition-all duration-200">
                            <h1>w</h1>
                        </span><span class="lg:hover:text-[90px] md:hover:text-[70px] transition-all duration-200">
                            <h1>o</h1>
                        </span><span class="lg:hover:text-[90px] md:hover:text-[70px] transition-all duration-200">
                            <h1>r</h1>
                        </span><span class="lg:hover:text-[90px] md:hover:text-[70px] transition-all duration-200">
                            <h1>l</h1>
                        </span><span class="lg:hover:text-[90px] md:hover:text-[70px] transition-all duration-200">
                            <h1>d</h1>
                        </span><span class="lg:hover:text-[90px] md:hover:text-[70px] transition-all duration-200">
                            <h1>!</h1>
                        </span>
                    </div>
                </div>
            </div>
            <NuxtLink to="#info">
                <svg class="size-40 text-zinc-300 hidden md:flex animate-wiggle cursor-pointer hover:scale-125 transition-all duration-200"
                    xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24">
                    <path fill="currentColor"
                        d="m12 19.164l6.207-6.207l-1.414-1.414L12 16.336l-4.793-4.793l-1.414 1.414zm0-5.65l6.207-6.207l-1.414-1.414L12 10.686L7.207 5.893L5.793 7.307z" />
                </svg>
            </NuxtLink>
        </div>
    </section>
    <article class="sticky ml-auto mr-[6%] top-[90%] w-min bg-zinc-200 rounded-lg p-1 z-50">
        <NuxtLink to="#home" class="">
            <svg class="text-neutral-900" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24">
                <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M12 5v14m6-8l-6-6m-6 6l6-6" />
            </svg>
        </NuxtLink>
    </article>
    <section id="info" class="max-w-6xl mx-[6%] lg:mx-auto pt-[100px]">
        <div class="flex flex-col items-center gap-3">
            <div class="relative inline-block">
                <p class="relative z-10 text-xs text-zinc-50">Про меня</p>
                <span class="absolute left-5 -top-1 -z-10 h-6 w-6 rounded-full bg-blue-500"></span>
            </div>
            <p class="text-2xl mt-[2px] font-bold text-zinc-50">Меня зовут Тимофей</p>
            <span class="w-16 border-t border-blue-500"></span>
            <p class="text-xs mt-[10px] max-w-3xl text-center text-zinc-50">Lorem ipsum dolor sit amet consectetur
                adipisicing elit.
                Commodi exercitationem numquam
                sapiente maiores fugit! Ut, dolorem autem, maxime nostrum quia nesciunt consequuntur recusandae quos
                dicta perspiciatis ea eveniet, culpa repellat!
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Architecto non odio repudiandae dolor quia
                ullam aperiam recusandae! Rem, soluta, officiis eveniet nihil libero, unde laudantium magnam aut sit
                voluptas laborum.
                sapiente maiores fugit! Ut, dolorem autem, maxime nostrum quia nesciunt consequuntur recusandae quos
                dicta perspiciatis ea eveniet, culpa repellat!
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Architecto non odio repudiandae dolor quia
                ullam aperiam recusandae! Rem, soluta, officiis eveniet nihil libero, unde laudantium magnam aut sit
            </p>
            <div class="flex flex-col gap-[20px] mt-[20px] items-center justify-start max-w-xl">
                <div class="flex gap-[30px] md:gap-[60px] lg:gap-[100px]">
                    <div class="w-1/2 flex flex-col gap-1">
                        <p class="text-[12px] text-zinc-50">Верстка макетов</p>
                        <p class="text-[9px] text-zinc-200">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                            Quis aperiam
                            repudiandae assumenda eaque
                            libero. Veritatis, similique! Totam quibusdam accusamus</p>
                    </div>
                    <div class="w-1/2 flex flex-col gap-1">
                        <p class="text-[12px] text-zinc-50">Мобильная адаптация</p>
                        <p class="text-[9px] text-zinc-200">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                            Explicabo
                            reprehenderit quam ipsum ea
                            cum sequi voluptatum</p>
                    </div>
                </div>
                <div class="flex gap-[30px] md:gap-[60px] lg:gap-[100px]">
                    <div class="w-1/2 flex flex-col gap-1">
                        <p class="text-[12px] text-zinc-50">Серверная разработка</p>
                        <p class="text-[9px] text-zinc-200">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                            Placeat fuga
                            facilis dignissimos error
                            natus, obcaecati nulla</p>
                    </div>
                    <div class="w-1/2 flex flex-col gap-1">
                        <p class="text-[12px] text-zinc-50">Веб-дизайн</p>
                        <p class="text-[9px] text-zinc-200">Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                            Repellat
                            dignissimos quisquam fugiat
                            culpa veritatis eos perspiciatis neque itaque</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section id="stack" class="max-w-6xl mx-[6%] lg:mx-auto mt-[100px] md:pt-[150px]">
        <div class="flex flex-col items-center gap-3">
            <div class="relative inline-block">
                <p class="relative z-10 text-xs text-zinc-50">Навыки</p>
                <span class="absolute -left-0.5 -top-1 -z-10 h-6 w-6 rounded-full bg-blue-500"></span>
            </div>
            <p class="text-2xl mt-[2px] font-bold text-zinc-50">Стек технологий</p>
            <span class="w-16 border-t border-blue-500"></span>
            <div
                class="flex gap-[15px] flex-wrap md:max-w-[645px] lg:max-w-[845px] w-max mx-auto max-w-[215px] mt-[50px]">
                <div
                    class="rounded-lg bg-[#222]/30 w-[100px] h-[100px] md:w-[150px] md:h-[150px] lg:w-[200px] lg:h-[200px] flex flex-col items-center justify-center gap-3 hover:scale-110 transition-all duration-200 cursor-pointer">
                    <img class="size-[40px] md:size-[60px]" src="https://cdn-icons-png.flaticon.com/256/174/174854.png"
                        loading="lazy">
                    <h2 class="text-white font-semibold text-sm">HTML5</h2>
                </div>
                <div
                    class="rounded-lg bg-[#222]/30 w-[100px] h-[100px] md:w-[150px] md:h-[150px] lg:w-[200px] lg:h-[200px] flex flex-col items-center justify-center gap-3 hover:scale-110 transition-all duration-200 cursor-pointer">
                    <img class="size-[40px] md:size-[60px]"
                        src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/CSS3_logo.svg/2048px-CSS3_logo.svg.png"
                        loading="lazy">
                    <h2 class="text-white font-semibold text-sm">CSS3</h2>
                </div>
                <div
                    class="rounded-lg bg-[#222]/30 w-[100px] h-[100px] md:w-[150px] md:h-[150px] lg:w-[200px] lg:h-[200px] flex flex-col items-center justify-center gap-3 hover:scale-110 transition-all duration-200 cursor-pointer">
                    <img class="size-[40px] md:size-[60px] scale-125"
                        src="https://static.vecteezy.com/system/resources/previews/027/127/463/non_2x/javascript-logo-javascript-icon-transparent-free-png.png"
                        loading="lazy">
                    <h2 class="text-white font-semibold text-sm">JS</h2>
                </div>
                <div
                    class="rounded-lg bg-[#222]/30 w-[100px] h-[100px] md:w-[150px] md:h-[150px] lg:w-[200px] lg:h-[200px] flex flex-col items-center justify-center gap-3 hover:scale-110 transition-all duration-200 cursor-pointer">
                    <img class="size-[40px] md:size-[60px]"
                        src="https://cdn.iconscout.com/icon/free/png-256/free-vue-logo-icon-download-in-svg-png-gif-file-formats--company-brand-world-logos-vol-5-pack-icons-282497.png?f=webp&w=256"
                        loading="lazy">
                    <h2 class="text-white font-semibold text-sm">VUE</h2>
                </div>
                <div
                    class="rounded-lg bg-[#222]/30 w-[100px] h-[100px] md:w-[150px] md:h-[150px] lg:w-[200px] lg:h-[200px] flex flex-col items-center justify-center gap-3 hover:scale-110 transition-all duration-200 cursor-pointer">
                    <img class="size-[40px] md:size-[60px] scale-150"
                        src="https://nuxt.com/assets/design-kit/icon-green.svg" loading="lazy">
                    <h2 class="text-white font-semibold text-sm">NUXT</h2>
                </div>
                <div
                    class="rounded-lg bg-[#222]/30 w-[100px] h-[100px] md:w-[150px] md:h-[150px] lg:w-[200px] lg:h-[200px] flex flex-col items-center justify-center gap-3 hover:scale-110 transition-all duration-200 cursor-pointer">
                    <img class="size-[40px] md:size-[60px]"
                        src="https://static-00.iconduck.com/assets.00/node-js-icon-1817x2048-g8tzf91e.png"
                        loading="lazy">
                    <h2 class="text-white font-semibold text-sm">NODE.JS</h2>
                </div>
                <div
                    class="rounded-lg bg-[#222]/30 w-[100px] h-[100px] md:w-[150px] md:h-[150px] lg:w-[200px] lg:h-[200px] flex flex-col items-center justify-center gap-3 hover:scale-110 transition-all duration-200 cursor-pointer">
                    <img class="size-[40px] md:size-[60px]"
                        src="https://static-00.iconduck.com/assets.00/mongodb-icon-1024x1024-jyklwn1x.png"
                        loading="lazy">
                    <h2 class="text-white font-semibold text-sm">MONGODB</h2>
                </div>
                <div
                    class="rounded-lg bg-[#222]/30 w-[100px] h-[100px] md:w-[150px] md:h-[150px] lg:w-[200px] lg:h-[200px] flex flex-col items-center justify-center gap-3 hover:scale-110 transition-all duration-200 cursor-pointer">
                    <img class="w-[40px] md:w-[80px]" src="../public/tailwind.png" loading="lazy">
                    <h2 class="text-white font-semibold text-sm pt-[10px]">TAILWIND</h2>
                </div>
            </div>
        </div>


        <div class="content mx-auto flex gap-[30px] relative justify-center my-[50px] flex-wrap">
            <div
                class="box relative py-[40px] w-[240px] bg-[#222]/30 flex justify-center flex-col items-center rounded-lg">
                <div
                    class="circle one relative w-[150px] h-[150px] rounded-full flex items-center justify-center flex-col transition-all duration-200 hover:scale-120 cursor-pointer">
                    <h2 class="result text-center relative text-[32px] transition-all duration-200 text-white">70<span
                            class="text-[18px]">%</span></h2>
                    <h3 class="desc relative">CSS</h3>
                </div>
            </div>

            <div
                class="box relative py-[40px] w-[240px] bg-[#222]/30 flex justify-center flex-col items-center rounded-lg">
                <div
                    class="circle two relative w-[150px] h-[150px] rounded-full flex items-center justify-center flex-col transition-transform duration-200 hover:scale-120 cursor-pointer">
                    <h2 class="result text-center relative text-[32px] transition-all duration-200 text-white">80<span
                            class="text-[18px]">%</span></h2>
                    <h3 class="desc relative">HTML</h3>
                </div>
            </div>

            <div
                class="box relative py-[40px] w-[240px] bg-[#222]/30 flex justify-center flex-col items-center rounded-lg">
                <div
                    class="circle three relative w-[150px] h-[150px] rounded-full flex items-center justify-center flex-col transition-transform duration-200 hover:scale-120 cursor-pointer">
                    <h2 class="result text-center relative text-[32px] transition-all duration-200 text-white">75<span
                            class="text-[18px]">%</span></h2>
                    <h3 class="desc relative">JS</h3>
                </div>
            </div>
        </div>
    </section>
    <section id="contacts" class="max-w-6xl mx-[6%] lg:mx-auto mt-[100px] md:pt-[150px] mb-[200px]">
        <div class="flex flex-col items-center">
            <p class="text-2xl mt-[2px] font-bold text-zinc-50">Контакты</p>
            <span class="w-13 border-t border-blue-500"></span>
            <div class="mt-[50px] flex flex-wrap mx-auto w-min md:w-max">
                <NuxtLink to="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
                    class="flex flex-col items-center justify-center size-[170px]">
                    <svg class="text-neutral-400" xmlns="http://www.w3.org/2000/svg" width="70" height="70"
                        viewBox="0 0 24 24"><!-- Icon from Material Symbols by Google - https://github.com/google/material-design-icons/blob/master/LICENSE -->
                        <path fill="currentColor"
                            d="M4 20q-.825 0-1.412-.587T2 18V6q0-.825.588-1.412T4 4h16q.825 0 1.413.588T22 6v12q0 .825-.587 1.413T20 20zm8-7.175q.125 0 .263-.038t.262-.112L19.6 8.25q.2-.125.3-.312t.1-.413q0-.5-.425-.75T18.7 6.8L12 11L5.3 6.8q-.45-.275-.875-.012T4 7.525q0 .25.1.438t.3.287l7.075 4.425q.125.075.263.113t.262.037" />
                    </svg>
                    <h3 class="text-xs text-neutral-400">exam@email.com</h3>
                </NuxtLink>
                <NuxtLink to="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
                    class="flex flex-col items-center justify-center size-[170px]">
                    <svg class="text-neutral-400 scale-120" xmlns="http://www.w3.org/2000/svg" width="70" height="70"
                        viewBox="0 0 24 24"><!-- Icon from BoxIcons Logo by Atisa - https://creativecommons.org/licenses/by/4.0/ -->
                        <path fill="currentColor"
                            d="M21.579 6.855c.14-.465 0-.806-.662-.806h-2.193c-.558 0-.813.295-.953.619c0 0-1.115 2.719-2.695 4.482c-.51.513-.743.675-1.021.675c-.139 0-.341-.162-.341-.627V6.855c0-.558-.161-.806-.626-.806H9.642c-.348 0-.558.258-.558.504c0 .528.79.65.871 2.138v3.228c0 .707-.127.836-.407.836c-.743 0-2.551-2.729-3.624-5.853c-.209-.607-.42-.852-.98-.852H2.752c-.627 0-.752.295-.752.619c0 .582.743 3.462 3.461 7.271c1.812 2.601 4.363 4.011 6.687 4.011c1.393 0 1.565-.313 1.565-.853v-1.966c0-.626.133-.752.574-.752c.324 0 .882.164 2.183 1.417c1.486 1.486 1.732 2.153 2.567 2.153h2.192c.626 0 .939-.313.759-.931c-.197-.615-.907-1.51-1.849-2.569c-.512-.604-1.277-1.254-1.51-1.579c-.325-.419-.231-.604 0-.976c.001.001 2.672-3.761 2.95-5.04" />
                    </svg>
                    <h3 class="text-xs text-neutral-400">vk.com/example</h3>
                </NuxtLink>
                <NuxtLink to="https://github.com/xazada13"
                    class="flex flex-col items-center justify-center size-[170px]">
                    <svg class="text-neutral-400 scale-90" xmlns="http://www.w3.org/2000/svg" width="70" height="70"
                        viewBox="0 0 24 24"><!-- Icon from BoxIcons Logo by Atisa - https://creativecommons.org/licenses/by/4.0/ -->
                        <path fill="currentColor" fill-rule="evenodd"
                            d="M12.026 2c-5.509 0-9.974 4.465-9.974 9.974c0 4.406 2.857 8.145 6.821 9.465c.499.09.679-.217.679-.481c0-.237-.008-.865-.011-1.696c-2.775.602-3.361-1.338-3.361-1.338c-.452-1.152-1.107-1.459-1.107-1.459c-.905-.619.069-.605.069-.605c1.002.07 1.527 1.028 1.527 1.028c.89 1.524 2.336 1.084 2.902.829c.091-.645.351-1.085.635-1.334c-2.214-.251-4.542-1.107-4.542-4.93c0-1.087.389-1.979 1.024-2.675c-.101-.253-.446-1.268.099-2.64c0 0 .837-.269 2.742 1.021a9.6 9.6 0 0 1 2.496-.336a9.6 9.6 0 0 1 2.496.336c1.906-1.291 2.742-1.021 2.742-1.021c.545 1.372.203 2.387.099 2.64c.64.696 1.024 1.587 1.024 2.675c0 3.833-2.33 4.675-4.552 4.922c.355.308.675.916.675 1.846c0 1.334-.012 2.41-.012 2.737c0 .267.178.577.687.479C19.146 20.115 22 16.379 22 11.974C22 6.465 17.535 2 12.026 2"
                            clip-rule="evenodd" />
                    </svg>
                    <h3 class="text-xs text-neutral-400">xazada13</h3>
                </NuxtLink>
            </div>
        </div>
    </section>

    <footer-app></footer-app>
</template>

<style>
:root {
    --red-color: #fc4040;
    --blue-color: rgb(0, 119, 255);
    --yellow-color: rgb(255, 196, 0);
}

h1,
h2,
h3,
p {
    font-family: "Martian Mono", monospace
}

html {
    scroll-behavior: smooth;
}

.circle::before {
    content: '';
    position: absolute;
    background-color: #25252b;
    inset: 10px;
    border-radius: 50%;
}

.circle:hover .result {
    font-size: 40px;
}

.circle.one {
    background: conic-gradient(from 0deg, var(--blue-color) 0%, var(--blue-color) 0% 70%, #333 70%, #333 100%);
}

.circle.one .result,
.circle.one .desc {
    color: var(--blue-color);
    text-shadow: 0px 0pc 10pc var(--blue-color);
}

.circle.two {
    background: conic-gradient(from 0deg, var(--red-color) 0%, var(--red-color) 0% 80%, #333 80%, #333 100%);
}

.circle.two .result,
.circle.two .desc {
    color: var(--red-color);
    text-shadow: 0px 0pc 10pc var(--red-color);
}

.circle.three {
    background: conic-gradient(from 0deg, var(--yellow-color) 0%, var(--yellow-color) 0% 75%, #333 75%, #333 100%);
}

.circle.three .result,
.circle.three .desc {
    color: var(--yellow-color);
    text-shadow: 0px 0pc 10pc var(--yellow-color);
}
</style>