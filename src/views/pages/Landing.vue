<script setup>
import { useLayout } from '@/layout/composables/layout';
import { computed } from 'vue';
import AppConfig from '@/layout/AppConfig.vue';

const { layoutConfig } = useLayout();

const smoothScroll = (id) => {
    document.querySelector(id).scrollIntoView({
        behavior: 'smooth'
    });
};


 const logoUrl = computed(() => {
    return `layout/images/${layoutConfig.darkTheme.value ? 'car' : 'car'}.png`;
}); 
</script>

<template>
    <div class="surface-0 flex justify-content-center">
        <div id="home" class="landing-wrapper overflow-hidden">
            <div class="py-4 px-4 mx-0 md:mx-6 lg:mx-8 lg:px-8 flex align-items-center justify-content-between relative lg:static mb-3">
                <a class="flex align-items-center" href="#"> <img :src="logoUrl" height="50" class="mr-0 lg:mr-2" /><span class="text-900 font-medium text-2xl line-height-3 mr-8">DDRent</span> </a>
                <a class="cursor-pointer block lg:hidden text-700 p-ripple" v-ripple v-styleclass="{ selector: '@next', enterClass: 'hidden', leaveToClass: 'hidden', hideOnOutsideClick: true }">
                    <i class="pi pi-bars text-4xl"></i>
                </a>
                <div class="align-items-center surface-0 flex-grow-1 justify-content-between hidden lg:flex absolute lg:static w-full left-0 px-6 lg:px-0 z-2" style="top: 120px">
                    <ul class="list-none p-0 m-0 flex lg:align-items-center select-none flex-column lg:flex-row cursor-pointer">
                        <li>
                            <a @click="smoothScroll('#hero')" class="flex m-0 md:ml-5 px-0 py-3 text-900 font-medium line-height-3 p-ripple" v-ripple>
                                <span>Anasayfa</span>
                            </a>
                        </li>
                        <li>
                            <a @click="smoothScroll('#features')" class="flex m-0 md:ml-5 px-0 py-3 text-900 font-medium line-height-3 p-ripple" v-ripple>
                                <span>Biz Kimiz ?</span>
                            </a>
                        </li>
                        <li>
                            <a @click="smoothScroll('#highlights')" class="flex m-0 md:ml-5 px-0 py-3 text-900 font-medium line-height-3 p-ripple" v-ripple>
                                <span>İletişim</span>
                            </a>
                        </li>
                        <li>
                            <a @click="smoothScroll('#pricing')" class="flex m-0 md:ml-5 px-0 py-3 text-900 font-medium line-height-3 p-ripple" v-ripple>
                                <span>Araçlarımız</span>
                            </a>
                        </li>
                    </ul>
                    <div class="flex justify-content-between lg:block border-top-1 lg:border-top-none surface-border py-3 lg:py-0 mt-3 lg:mt-0">
                    
                        <Button label="Giriş" class="p-button-rounded border-none ml-5 font-light text-white line-height-2 bg-blue-500"></Button>
                    </div>
                </div>
            </div>

            <div
                id="hero"
                class="flex flex-column pt-4 px-4 lg:px-8 overflow-hidden"
                style="background: linear-gradient(0deg, rgba(255, 255, 255, 0.2), rgba(255, 255, 255, 0.2)), radial-gradient(77.36% 256.97% at 77.36% 57.52%, rgb(238, 239, 175) 0%, rgb(195, 227, 250) 100%); clip-path: ellipse(150% 87% at 93% 13%)"
            >
                <div class="mx-4 md:mx-8 mt-0 md:mt-4">
                    <h1 class="text-6xl font-bold text-gray-900 line-height-2"><span class="font-light block">Yolculuğunuza eşlik eden güvenilir araç kiralama.</span>Geniş araç filomuzla her ihtiyaca uygun seçenekler.</h1>
                    <p class="font-normal text-2xl line-height-3 md:mt-3 text-gray-700">Profesyonel ve güler yüzlü ekip tarafından müşteri memnuniyeti odaklı hizmet.</p>
                    <Button label="Araçlarımız" class="p-button-rounded text-xl border-none mt-5 bg-blue-500 font-normal text-white line-height-3 px-3"></Button>
                </div>
                <div class="flex justify-content-center md:justify-content-end">
                    <img style="object-fit: 'containt'; " src="../../../public/layout/images/cars.png" width="250" height="350" alt="Hero Image" class="w-9 md:w-auto" />
                </div>
            </div>

            <div id="features" class="py-4 px-4 lg:px-8 mt-5 mx-0 lg:mx-8">
                <div class="grid justify-content-center">
                    <div class="col-12 text-center mt-8 mb-4">
                        <h2 class="text-900 font-normal mb-2">Biz Kimiz ?</h2>
                        <span class="text-600 text-2xl">Biraz kendimizden bahsedelim</span>
                    </div>

                    <div class="col-12 md:col-12 lg:col-4 p-0 lg:pr-5 lg:pb-5 mt-4 lg:mt-0">
                        <div
                            style="height: 160px; padding: 2px; border-radius: 10px; background: linear-gradient(90deg, rgba(253, 228, 165, 0.2), rgba(187, 199, 205, 0.2)), linear-gradient(180deg, rgba(253, 228, 165, 0.2), rgba(187, 199, 205, 0.2))"
                        >
                            <div class="p-3 surface-card h-full" style="border-radius: 8px">
                                <div class="flex align-items-center justify-content-center bg-yellow-200 mb-3" style="width: 3.5rem; height: 3.5rem; border-radius: 10px">
                                    <i class="pi pi-fw pi-users text-2xl text-yellow-700"></i>
                                </div>
                                <h5 class="mb-2 text-900">Yıl 2018</h5>
                                <span class="text-600">2018'de kurulmuş olan bir aile şirketiyiz.</span>
                            </div>
                        </div>
                    </div>

                    <div class="col-12 md:col-12 lg:col-4 p-0 lg:pr-5 lg:pb-5 mt-4 lg:mt-0">
                        <div
                            style="height: 160px; padding: 2px; border-radius: 10px; background: linear-gradient(90deg, rgba(145, 226, 237, 0.2), rgba(251, 199, 145, 0.2)), linear-gradient(180deg, rgba(253, 228, 165, 0.2), rgba(172, 180, 223, 0.2))"
                        >
                            <div class="p-3 surface-card h-full" style="border-radius: 8px">
                                <div class="flex align-items-center justify-content-center bg-cyan-200 mb-3" style="width: 3.5rem; height: 3.5rem; border-radius: 10px">
                                    <i class="pi pi-fw pi-star text-2xl text-cyan-700"></i>
                                </div>
                                <h5 class="mb-2 text-900">En İyisi Olmak</h5>
                                <span class="text-600">Güvenilir ve sorunsuz araç kiralama deneyimi sağlamak için çalışıyoruz.</span>
                            </div>
                        </div>
                    </div>

                    <div class="col-12 md:col-12 lg:col-4 p-0 lg:pb-5 mt-4 lg:mt-0">
                        <div
                            style="height: 160px; padding: 2px; border-radius: 10px; background: linear-gradient(90deg, rgba(145, 226, 237, 0.2), rgba(172, 180, 223, 0.2)), linear-gradient(180deg, rgba(172, 180, 223, 0.2), rgba(246, 158, 188, 0.2))"
                        >
                            <div class="p-3 surface-card h-full" style="border-radius: 8px">
                                <div class="flex align-items-center justify-content-center bg-indigo-200" style="width: 3.5rem; height: 3.5rem; border-radius: 10px">
                                    <i class="pi pi-fw pi-map text-2xl text-indigo-700"></i>
                                </div>
                                <h5 class="mb-2 text-900">Kültürel İletişim</h5>
                                <span class="text-600">Yerel ve uluslararası müşterilere geniş kapsamlı hizmetler sunuyoruz.</span>
                            </div>
                        </div>
                    </div>


                    <div class="col-12 md:col-12 lg:col-4 p-0 lg:pr-5 mt-4 lg:mt-0">
                        <div
                            style="height: 160px; padding: 2px; border-radius: 10px; background: linear-gradient(90deg, rgba(145, 210, 204, 0.2), rgba(160, 210, 250, 0.2)), linear-gradient(180deg, rgba(187, 199, 205, 0.2), rgba(145, 210, 204, 0.2))"
                        >
                            <div class="p-3 surface-card h-full" style="border-radius: 8px">
                                <div class="flex align-items-center justify-content-center bg-teal-200 mb-3" style="width: 3.5rem; height: 3.5rem; border-radius: 10px">
                                    <i class="pi pi-fw pi-shopping-cart text-2xl text-teal-700"></i>
                                </div>
                                <h5 class="mb-2 text-900">Uygun Fiyatlar</h5>
                                <span class="text-600">En iyi hizmet, en iyi fiyat, tek adres</span>
                            </div>
                        </div>
                    </div>

                    <div class="col-12 md:col-12 lg:col-4 p-0 lg:pr-5 mt-4 lg:mt-0">
                        <div
                            style="height: 160px; padding: 2px; border-radius: 10px; background: linear-gradient(90deg, rgba(145, 210, 204, 0.2), rgba(212, 162, 221, 0.2)), linear-gradient(180deg, rgba(251, 199, 145, 0.2), rgba(160, 210, 250, 0.2))"
                        >
                            <div class="p-3 surface-card h-full" style="border-radius: 8px">
                                <div class="flex align-items-center justify-content-center bg-blue-200 mb-3" style="width: 3.5rem; height: 3.5rem; border-radius: 10px">
                                    <i class="pi pi-fw pi-globe text-2xl text-blue-700"></i>
                                </div>
                                <h5 class="mb-2 text-900">7/24 Müşteri Desteği</h5>
                                <span class="text-600">365g/24s sizler için çalışmaktayız.</span>
                            </div>
                        </div>
                    </div>

                    <div class="col-12 md:col-12 lg:col-4 p-0 lg-4 mt-4 lg:mt-0">
                        <div
                            style="height: 160px; padding: 2px; border-radius: 10px; background: linear-gradient(90deg, rgba(160, 210, 250, 0.2), rgba(212, 162, 221, 0.2)), linear-gradient(180deg, rgba(246, 158, 188, 0.2), rgba(212, 162, 221, 0.2))"
                        >
                            <div class="p-3 surface-card h-full" style="border-radius: 8px">
                                <div class="flex align-items-center justify-content-center bg-purple-200 mb-3" style="width: 3.5rem; height: 3.5rem; border-radius: 10px">
                                    <i class="pi pi-fw pi-car text-2xl text-purple-700"></i>
                                </div>
                                <h5 class="mb-2 text-900">Hızlı Ulaşım</h5>
                                <span class="text-600">Adamıza ister gemi yolu, ister hava yolu ile gelin. Aracanız kapıda sizi bekliyor olacak !</span>
                            </div>
                        </div>
                    </div>

                    <div
                        class="col-12 mt-8 mb-8 p-2 md:p-8"
                        style="border-radius: 20px; background: linear-gradient(0deg, rgba(255, 255, 255, 0.6), rgba(255, 255, 255, 0.6)), radial-gradient(77.36% 256.97% at 77.36% 57.52%, #efe1af 0%, #c3dcfa 100%)"
                    >
                        <div class="flex flex-column justify-content-center align-items-center text-center px-3 py-3 md:py-0">
                            
                            <p class="text-gray-900 sm:line-height-2 md:line-height-4 text-2xl mt-4" style="max-width: 800px">
                                Her gün daha iyisi için çalışıyoruz, en iyiyi sunmaktan gurur duyuyoruz.
                            </p>
                            <img src="../../../public/layout/images/car.png" width="100" height="100" class="mt-4" />
                        </div>
                    </div>
                </div>
            </div>

            <div id="highlights" class="py-4 px-4 lg:px-8 mx-0 my-6 lg:mx-8">
                <div class="text-center">
                    <h2 class="text-900 font-normal mb-2">Her Zaman Her Yerde</h2>
                    <span class="text-600 text-2xl">Web sitemiz ile bize her yerden ulaşın !</span>
                </div>

                <div class="grid mt-8 pb-2 md:pb-8">
                    <div class="flex justify-content-center col-12 lg:col-6 bg-purple-100 p-0 flex-order-1 lg:flex-order-0" style="border-radius: 8px">
                        <img src="/demo/images/landing/mockup.svg" class="w-11" alt="mockup mobile" />
                    </div>

                    <div class="col-12 lg:col-6 my-auto flex flex-column lg:align-items-end text-center lg:text-right">
                        <div class="flex align-items-center justify-content-center bg-purple-200 align-self-center lg:align-self-end" style="width: 4.2rem; height: 4.2rem; border-radius: 10px">
                            <i class="pi pi-fw pi-mobile text-5xl text-purple-700"></i>
                        </div>
                        <h2 class="line-height-1 text-900 text-4xl font-normal">Mobil uyumluluk desen var !</h2>
                        <span class="text-700 text-2xl line-height-3 ml-0 md:ml-2" style="max-width: 650px"
                            >Keşfetmeye hazır olun! Mobil uyumlu benzersiz projemizle her an, her yerde sınırsız erişim keyfini yaşayın. Pratik ve kullanıcı dostu tasarımı sayesinde projemize istediğiniz cihazdan kolayca ulaşabilir, hayatınızı daha da kolaylaştırabilirsiniz. Daha fazlası için hemen tıklayın ve sizi müthiş bir deneyime davet edelim!</span
                        >
                    </div>
                </div>

                <div class="grid my-8 pt-2 md:pt-8">
                    <div class="col-12 lg:col-6 my-auto flex flex-column text-center lg:text-left lg:align-items-start">
                        <div class="flex align-items-center justify-content-center bg-yellow-200 align-self-center lg:align-self-start" style="width: 4.2rem; height: 4.2rem; border-radius: 10px">
                            <i class="pi pi-fw pi-desktop text-5xl text-yellow-700"></i>
                        </div>
                        <h2 class="line-height-1 text-900 text-4xl font-normal">Özelleştirilmiş raporlama hizmeti...</h2>
                        <span class="text-700 text-2xl line-height-3 mr-0 md:mr-2" style="max-width: 650px"
                            >Kapsamlı ve özelleştirilebilir raporlama özelliği sayesinde verilerinizi istediğiniz gibi analiz edin, en değerli bilgilere anında erişin. Araçlarınızın ve randevularınızın ilerleyişini kolayca takip edin ve verileri dilediğiniz şekilde sunarak daha bilinçli kararlar alın. Raporlama sürecini zahmetsizce yönetin ve işinizin başarısına katkıda bulunun!</span
                        >
                    </div>

                    <div class="flex justify-content-end flex-order-1 sm:flex-order-2 col-12 lg:col-6 bg-yellow-100 p-0" style="border-radius: 8px">
                        <img src="/demo/images/landing/mockup-desktop.svg" class="w-11" alt="mockup" />
                    </div>
                </div>
            </div>

            <div id="pricing" class="py-4 px-4 lg:px-8 my-2 md:my-4">
                <div class="text-center">
                    <h2 class="text-900 font-normal mb-2">Araçlarımız</h2>
                    <span class="text-600 text-2xl">Ekonomik ve lüks araçlar arasından tercih yapma imkanı!</span>
                </div>

                <div class="grid justify-content-between mt-8 md:mt-0">
                    <div class="col-12 lg:col-4 p-0 md:p-3">
                        <div class="p-3 flex flex-column border-200 pricing-card cursor-pointer border-2 hover:border-primary transition-duration-300 transition-all" style="border-radius: 10px">
                            <h3 class="text-900 text-center my-5">Suzuki Swift 2018</h3>
                            <img src="../../../public/layout/images/suzuki.png" class="w-10 h-10 mx-auto"/>
                            

                            <div class="my-5 text-center">
                                <span class="text-5xl font-bold mr-2 text-900">$0</span>
                                <span class="text-600">Günlük</span>
                                <Button label="Get Started" class="block mx-auto mt-4 p-button-rounded border-none ml-3 font-light line-height-2 bg-blue-500 text-white"></Button>
                            </div>
                            <Divider class="w-full bg-surface-200"></Divider>
                            <ul class="my-5 list-none p-0 flex text-900 flex-column">
                                <li class="py-2">
                                    <i class="pi pi-fw pi-check text-xl text-cyan-500 mr-2"></i>
                                    <span class="text-xl line-height-3">1300CC Benzin Motor</span>
                                </li>
                                <li class="py-2">
                                    <i class="pi pi-fw pi-check text-xl text-cyan-500 mr-2"></i>
                                    <span class="text-xl line-height-3">4 Kişilik</span>
                                </li>
                            
                                <li class="py-2">
                                    <i class="pi pi-fw pi-check text-xl text-cyan-500 mr-2"></i>
                                    <span class="text-xl line-height-3">Ücretsiz teslim</span>
                                </li>
                            </ul>
                        </div>
                    </div>

                    <div class="col-12 lg:col-4 p-0 md:p-3 mt-4 md:mt-0">
                        <div class="p-3 flex flex-column border-200 pricing-card cursor-pointer border-2 hover:border-primary transition-duration-300 transition-all" style="border-radius: 10px">
                            <h3 class="text-900 text-center my-5">Mercedes-Benz E-Class </h3>
                            <img src="../../../public/layout/images/mercedes.png" class="w-10 h-10 mx-auto" />
                            <div class="my-5 text-center">
                                <span class="text-5xl font-bold mr-2 text-900">$1</span>
                                <span class="text-600">Günlük</span>
                                <Button label="Try Free" class="block mx-auto mt-4 p-button-rounded border-none ml-3 font-light line-height-2 bg-blue-500 text-white"></Button>
                            </div>
                            <Divider class="w-full bg-surface-200"></Divider>
                            <ul class="my-5 list-none p-0 flex text-900 flex-column">
                                <li class="py-2">
                                    <i class="pi pi-fw pi-check text-xl text-cyan-500 mr-2"></i>
                                    <span class="text-xl line-height-3">2500CC Dizel Motor</span>
                                </li>
                                <li class="py-2">
                                    <i class="pi pi-fw pi-check text-xl text-cyan-500 mr-2"></i>
                                    <span class="text-xl line-height-3">5 Kişilik</span>
                                </li>
                            
                                <li class="py-2">
                                    <i class="pi pi-fw pi-check text-xl text-cyan-500 mr-2"></i>
                                    <span class="text-xl line-height-3">Ücretsiz teslim</span>
                                </li>
                            </ul>
                        </div>
                    </div>

                    <div class="col-12 lg:col-4 p-0 md:p-3 mt-4 md:mt-0">
                        <div class="p-3 flex flex-column border-200 pricing-card cursor-pointer border-2 hover:border-primary transition-duration-300 transition-all" style="border-radius: 10px">
                            <h3 class="text-900 text-center my-5">Jeep Grand Cherokee 2017</h3>
                            <img src="../../../public/layout/images/jeep.png" class="w-10 h-10 mx-auto"/>
                            <div class="my-5 text-center">
                                <span class="text-5xl font-bold mr-2 text-900">$1</span>
                                <span class="text-600">Günlük</span>
                                <Button label="Try Free" class="block mx-auto mt-4 p-button-rounded border-none ml-3 font-light line-height-2 bg-blue-500 text-white"></Button>
                            </div>
                            <Divider class="w-full bg-surface-200"></Divider>
                            <ul class="my-5 list-none p-0 flex text-900 flex-column">
                                <li class="py-2">
                                    <i class="pi pi-fw pi-check text-xl text-cyan-500 mr-2"></i>
                                    <span class="text-xl line-height-3">3000CC Dizel Motor</span>
                                </li>
                                <li class="py-2">
                                    <i class="pi pi-fw pi-check text-xl text-cyan-500 mr-2"></i>
                                    <span class="text-xl line-height-3">5 Kişilik</span>
                                </li>
                            
                                <li class="py-2">
                                    <i class="pi pi-fw pi-check text-xl text-cyan-500 mr-2"></i>
                                    <span class="text-xl line-height-3">Ücretsiz teslim</span>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>

            <div class="py-4 px-4 mx-0 mt-8 lg:mx-8">
                <div class="grid justify-content-between">
                    <div class="col-12 md:col-2" style="margin-top: -1.5rem">
                        <a @click="smoothScroll('#home')" class="flex flex-wrap align-items-center justify-content-center md:justify-content-start md:mb-0 mb-3 cursor-pointer">
                            <img :src="logoUrl" alt="footer sections" width="50" height="50" class="mr-2" />
                            <h4 class="font-medium text-3xl text-900">DDRent a Car</h4>
                        </a>
                    </div>

                    <div class="col-12 md:col-10 lg:col-7">
                        <div class="grid text-center md:text-left">
                            <div class="col-12 md:col-3">
                                <h4 @click="smoothScroll('#hero')" class="font-medium text-2xl line-height-3 mb-3 text-900">Anasayfa</h4>
                            </div>

                            <div class="col-12 md:col-3 mt-4 md:mt-0">
                                
                                <h4 @click="smoothScroll('#features')" class="font-medium text-2xl line-height-3 mb-3 text-900">Biz Kimiz ?</h4>
                                
                            </div>

                            <div class="col-12 md:col-3 mt-4 md:mt-0">
                                <h4 @click="smoothScroll('#highlights')" class="font-medium text-2xl line-height-3 mb-3 text-900">İletişim</h4>
                               
                            </div>

                            <div class="col-12 md:col-3 mt-4 md:mt-0">
                                <h4 @click="smoothScroll('#pricing')" class="font-medium text-2xl line-height-3 mb-3 text-900">Araçlarımız</h4>
                            
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <AppConfig simple />
</template>

<!-- <style scoped>
#hero {
    background: linear-gradient(0deg, rgba(255, 255, 255, 0.2), rgba(255, 255, 255, 0.2)), radial-gradient(77.36% 256.97% at 77.36% 57.52%, #eeefaf 0%, #c3e3fa 100%);
    height: 700px;
    overflow: hidden;
}

@media screen and (min-width: 768px) {
    #hero {
        -webkit-clip-path: ellipse(150% 87% at 93% 13%);
        clip-path: ellipse(150% 87% at 93% 13%);
        height: 530px;
    }
}

@media screen and (min-width: 1300px) {
    #hero > img {
        position: absolute;
    }

    #hero > div > p {
        max-width: 450px;
    }
}

@media screen and (max-width: 1300px) {
    #hero {
        height: 600px;
    }

    #hero > img {
        position: static;
        transform: scale(1);
        margin-left: auto;
    }

    #hero > div {
        width: 100%;
    }

    #hero > div > p {
        width: 100%;
        max-width: 100%;
    }
}
</style> -->
