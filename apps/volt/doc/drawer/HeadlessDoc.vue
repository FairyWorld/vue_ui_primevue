<template>
    <DocSectionText v-bind="$attrs">
        <p>Headless mode is enabled by defining a <i>container</i> slot that lets you implement entire UI instead of the default elements.</p>
    </DocSectionText>
    <div class="card flex justify-center">
        <Drawer v-model:visible="visible" :modal="false">
            <template #container="{ closeCallback }">
                <div class="flex flex-col h-full">
                    <div class="flex items-center justify-between px-6 pt-4 shrink-0">
                        <span class="inline-flex items-center gap-2">
                            <svg width="66" height="30" viewBox="0 0 87 40" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M86.2669 20.7848C86.2669 20.9341 86.2243 21.0515 86.1389 21.1368C86.0536 21.2221 85.9363 21.2648 85.7869 21.2648H83.1309C83.0243 21.2648 82.9709 21.3181 82.9709 21.4248V26.4488C82.9709 27.5155 83.3549 28.0488 84.1229 28.0488H85.3069C85.4563 28.0488 85.5736 28.0915 85.6589 28.1768C85.7443 28.2621 85.7869 28.3795 85.7869 28.5288V32.6248C85.7869 32.9235 85.6269 33.0941 85.3069 33.1368C84.4749 33.2008 83.6749 33.2328 82.9069 33.2328C80.9656 33.2328 79.5363 32.9341 78.6189 32.3368C77.7016 31.7395 77.2323 30.6088 77.2109 28.9448V21.4248C77.2109 21.3181 77.1576 21.2648 77.0509 21.2648H75.3229C75.1736 21.2648 75.0563 21.2221 74.9709 21.1368C74.8856 21.0515 74.8429 20.9341 74.8429 20.7848V16.9448C74.8429 16.7955 74.8856 16.6781 74.9709 16.5928C75.0563 16.5075 75.1736 16.4648 75.3229 16.4648H77.0509C77.1576 16.4648 77.2109 16.4115 77.2109 16.3048V12.4648C77.2109 12.3155 77.2536 12.1981 77.3389 12.1128C77.4243 12.0275 77.5416 11.9848 77.6909 11.9848H82.4909C82.6403 11.9848 82.7576 12.0275 82.8429 12.1128C82.9283 12.1981 82.9709 12.3155 82.9709 12.4648V16.3048C82.9709 16.4115 83.0243 16.4648 83.1309 16.4648H85.7869C85.9363 16.4648 86.0536 16.5075 86.1389 16.5928C86.2243 16.6781 86.2669 16.7955 86.2669 16.9448V20.7848Z"
                                    fill="var(--p-primary-color)"
                                />
                                <path
                                    d="M67.7419 33.1048C67.5926 33.1048 67.4752 33.0621 67.3899 32.9768C67.3046 32.8915 67.2619 32.7741 67.2619 32.6248V11.1848C67.2619 11.0355 67.3046 10.9181 67.3899 10.8328C67.4752 10.7475 67.5926 10.7048 67.7419 10.7048H72.7979C72.9472 10.7048 73.0646 10.7475 73.1499 10.8328C73.2352 10.9181 73.2779 11.0355 73.2779 11.1848V32.6248C73.2779 32.7741 73.2352 32.8915 73.1499 32.9768C73.0646 33.0621 72.9472 33.1048 72.7979 33.1048H67.7419Z"
                                    fill="var(--p-primary-color)"
                                />
                                <path
                                    d="M57.2902 33.3608C55.2635 33.3608 53.5462 32.8168 52.1382 31.7288C50.7515 30.6408 49.8342 29.1688 49.3862 27.3128C49.1728 26.5448 49.0662 25.6915 49.0662 24.7528C49.0662 23.7075 49.1942 22.7581 49.4502 21.9048C49.9622 20.1341 50.9008 18.7475 52.2662 17.7448C53.6528 16.7208 55.3382 16.2088 57.3222 16.2088C59.3062 16.2088 60.9702 16.7208 62.3142 17.7448C63.6795 18.7475 64.6182 20.1128 65.1302 21.8408C65.3862 22.7368 65.5142 23.6861 65.5142 24.6888C65.5142 25.4995 65.4288 26.3101 65.2582 27.1208C64.8102 29.0408 63.8822 30.5661 62.4742 31.6968C61.0875 32.8061 59.3595 33.3608 57.2902 33.3608ZM57.2902 28.2088C57.8448 28.2088 58.2928 28.0275 58.6342 27.6648C58.9755 27.2808 59.2102 26.7795 59.3382 26.1608C59.4235 25.7555 59.4662 25.2755 59.4662 24.7208C59.4662 24.2301 59.4128 23.7395 59.3062 23.2488C58.9862 21.9901 58.3142 21.3608 57.2902 21.3608C56.2235 21.3608 55.5515 21.9901 55.2742 23.2488C55.1675 23.6115 55.1142 24.1021 55.1142 24.7208C55.1142 25.2755 55.1568 25.7555 55.2422 26.1608C55.5622 27.5261 56.2448 28.2088 57.2902 28.2088Z"
                                    fill="var(--p-primary-color)"
                                />
                                <path
                                    d="M37.5712 33.1048C37.4432 33.1048 37.3258 33.0728 37.2192 33.0088C37.1125 32.9235 37.0485 32.8168 37.0272 32.6888L30.7232 11.2488C30.7018 11.2061 30.6912 11.1528 30.6912 11.0888C30.6912 10.8328 30.8405 10.7048 31.1392 10.7048H36.6112C36.8885 10.7048 37.0592 10.8435 37.1232 11.1208L40.3232 24.6248C40.3445 24.7101 40.3765 24.7528 40.4192 24.7528C40.4618 24.7528 40.4938 24.7101 40.5152 24.6248L43.6192 11.1208C43.6832 10.8435 43.8538 10.7048 44.1312 10.7048H49.4752C49.6458 10.7048 49.7632 10.7581 49.8272 10.8648C49.9125 10.9501 49.9338 11.0781 49.8912 11.2488L43.5232 32.6888C43.5018 32.8168 43.4378 32.9235 43.3312 33.0088C43.2245 33.0728 43.1072 33.1048 42.9792 33.1048H37.5712Z"
                                    fill="var(--p-primary-color)"
                                />
                                <path
                                    fill-rule="evenodd"
                                    clip-rule="evenodd"
                                    d="M4.043 15.0334L8.03101 16.6142H10.7377L11.713 0.106103C11.7195 -0.00249146 11.5724 -0.0417968 11.5238 0.0555237L4.043 15.0334ZM2.55847 23.2515H0.100129C0.0258101 23.2515 -0.0225409 23.1733 0.0106666 23.1068L2.30586 18.5114L4.69286 17.9483L2.55847 21.1927V23.2515ZM17.4689 29.2273L10.9293 39.2178C10.8699 39.3085 10.7288 39.2531 10.747 39.1462L13.4481 23.2515H4.44864V21.8287H4.46887L6.90673 17.9375L8.42408 18.9076H13.5137L15.031 17.9375L17.4689 21.8287V29.2273ZM20.0244 17.8162H24.7534C24.8329 17.8162 24.8806 17.9044 24.8371 17.9709L19.3793 26.3088V21.1927L17.2449 17.9483L19.3793 18.595L20.0244 17.8162Z"
                                    fill="var(--p-primary-color)"
                                />
                            </svg>
                        </span>
                        <span>
                            <Button type="button" @click="closeCallback" icon="pi pi-times" rounded outlined></Button>
                        </span>
                    </div>
                    <div class="overflow-y-auto">
                        <ul class="list-none p-4 m-0">
                            <li>
                                <div
                                    v-styleclass="{
                                        selector: '@next',
                                        enterFromClass: 'hidden',
                                        enterActiveClass: 'animate-slidedown',
                                        leaveToClass: 'hidden',
                                        leaveActiveClass: 'animate-slideup'
                                    }"
                                    class="p-4 flex items-center justify-between text-surface-500 dark:text-surface-400 cursor-pointer"
                                >
                                    <span class="font-medium">FAVORITES</span>
                                    <i class="pi pi-chevron-down"></i>
                                </div>
                                <ul class="list-none p-0 m-0 overflow-hidden">
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-home mr-2"></i>
                                            <span class="font-medium">Dashboard</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-bookmark mr-2"></i>
                                            <span class="font-medium">Bookmarks</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a
                                            v-styleclass="{
                                                selector: '@next',
                                                enterFromClass: 'hidden',
                                                enterActiveClass: 'animate-slidedown',
                                                leaveToClass: 'hidden',
                                                leaveActiveClass: 'animate-slideup'
                                            }"
                                            class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors"
                                        >
                                            <i class="pi pi-chart-line mr-2"></i>
                                            <span class="font-medium">Reports</span>
                                            <i class="pi pi-chevron-down ml-auto"></i>
                                        </a>
                                        <ul class="list-none py-0 pl-4 pr-0 m-0 hidden overflow-y-hidden transition-all duration-[400ms] ease-in-out">
                                            <li>
                                                <a
                                                    v-styleclass="{
                                                        selector: '@next',
                                                        enterFromClass: 'hidden',
                                                        enterActiveClass: 'animate-slidedown',
                                                        leaveToClass: 'hidden',
                                                        leaveActiveClass: 'animate-slideup'
                                                    }"
                                                    class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors"
                                                >
                                                    <i class="pi pi-chart-line mr-2"></i>
                                                    <span class="font-medium">Revenue</span>
                                                    <i class="pi pi-chevron-down ml-auto"></i>
                                                </a>
                                                <ul class="list-none py-0 pl-4 pr-0 m-0 hidden overflow-y-hidden transition-all duration-[400ms] ease-in-out">
                                                    <li>
                                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                                            <i class="pi pi-table mr-2"></i>
                                                            <span class="font-medium">View</span>
                                                        </a>
                                                    </li>
                                                    <li>
                                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                                            <i class="pi pi-search mr-2"></i>
                                                            <span class="font-medium">Search</span>
                                                        </a>
                                                    </li>
                                                </ul>
                                            </li>
                                            <li>
                                                <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                                    <i class="pi pi-chart-line mr-2"></i>
                                                    <span class="font-medium">Expenses</span>
                                                </a>
                                            </li>
                                        </ul>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-users mr-2"></i>
                                            <span class="font-medium">Team</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-comments mr-2"></i>
                                            <span class="font-medium">Messages</span>
                                            <span class="inline-flex items-center justify-center ml-auto bg-primary text-primary-contrast rounded-full" style="min-width: 1.5rem; height: 1.5rem">3</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-calendar mr-2"></i>
                                            <span class="font-medium">Calendar</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-cog mr-2"></i>
                                            <span class="font-medium">Settings</span>
                                        </a>
                                    </li>
                                </ul>
                            </li>
                        </ul>
                        <ul class="list-none p-4 m-0">
                            <li>
                                <div
                                    v-styleclass="{
                                        selector: '@next',
                                        enterFromClass: 'hidden',
                                        enterActiveClass: 'animate-slidedown',
                                        leaveToClass: 'hidden',
                                        leaveActiveClass: 'animate-slideup'
                                    }"
                                    class="p-4 flex items-center justify-between text-surface-500 dark:text-surface-400 cursor-pointer"
                                >
                                    <span class="font-medium">APPLICATION</span>
                                    <i class="pi pi-chevron-down"></i>
                                </div>
                                <ul class="list-none p-0 m-0 overflow-hidden">
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-folder mr-2"></i>
                                            <span class="font-medium">Projects</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-chart-bar mr-2"></i>
                                            <span class="font-medium">Performance</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-cog mr-2"></i>
                                            <span class="font-medium">Settings</span>
                                        </a>
                                    </li>
                                </ul>
                            </li>
                        </ul>
                    </div>
                    <div class="mt-auto">
                        <hr class="mb-4 mx-4 border-t border-0 border-surface-200 dark:border-surface-700" />
                        <a class="m-4 flex items-center cursor-pointer p-4 gap-2 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                            <Avatar image="https://primefaces.org/cdn/primevue/images/avatar/amyelsner.png" shape="circle" />
                            <span class="font-bold">Amy Elsner</span>
                        </a>
                    </div>
                </div>
            </template>
        </Drawer>
        <Button icon="pi pi-bars" @click="visible = true" />
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import Avatar from '@/volt/Avatar.vue';
import Button from '@/volt/Button.vue';
import Drawer from '@/volt/Drawer.vue';
import { ref } from 'vue';

const visible = ref(false);

const code = ref(`
<template>
    <div class="card flex justify-center">
        <Drawer v-model:visible="visible" :modal="false">
            <template #container="{ closeCallback }">
                <div class="flex flex-col h-full">
                    <div class="flex items-center justify-between px-6 pt-4 shrink-0">
                        <span class="inline-flex items-center gap-2">
                            <svg width="66" height="30" viewBox="0 0 87 40" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M86.2669 20.7848C86.2669 20.9341 86.2243 21.0515 86.1389 21.1368C86.0536 21.2221 85.9363 21.2648 85.7869 21.2648H83.1309C83.0243 21.2648 82.9709 21.3181 82.9709 21.4248V26.4488C82.9709 27.5155 83.3549 28.0488 84.1229 28.0488H85.3069C85.4563 28.0488 85.5736 28.0915 85.6589 28.1768C85.7443 28.2621 85.7869 28.3795 85.7869 28.5288V32.6248C85.7869 32.9235 85.6269 33.0941 85.3069 33.1368C84.4749 33.2008 83.6749 33.2328 82.9069 33.2328C80.9656 33.2328 79.5363 32.9341 78.6189 32.3368C77.7016 31.7395 77.2323 30.6088 77.2109 28.9448V21.4248C77.2109 21.3181 77.1576 21.2648 77.0509 21.2648H75.3229C75.1736 21.2648 75.0563 21.2221 74.9709 21.1368C74.8856 21.0515 74.8429 20.9341 74.8429 20.7848V16.9448C74.8429 16.7955 74.8856 16.6781 74.9709 16.5928C75.0563 16.5075 75.1736 16.4648 75.3229 16.4648H77.0509C77.1576 16.4648 77.2109 16.4115 77.2109 16.3048V12.4648C77.2109 12.3155 77.2536 12.1981 77.3389 12.1128C77.4243 12.0275 77.5416 11.9848 77.6909 11.9848H82.4909C82.6403 11.9848 82.7576 12.0275 82.8429 12.1128C82.9283 12.1981 82.9709 12.3155 82.9709 12.4648V16.3048C82.9709 16.4115 83.0243 16.4648 83.1309 16.4648H85.7869C85.9363 16.4648 86.0536 16.5075 86.1389 16.5928C86.2243 16.6781 86.2669 16.7955 86.2669 16.9448V20.7848Z"
                                    fill="var(--p-primary-color)"
                                />
                                <path
                                    d="M67.7419 33.1048C67.5926 33.1048 67.4752 33.0621 67.3899 32.9768C67.3046 32.8915 67.2619 32.7741 67.2619 32.6248V11.1848C67.2619 11.0355 67.3046 10.9181 67.3899 10.8328C67.4752 10.7475 67.5926 10.7048 67.7419 10.7048H72.7979C72.9472 10.7048 73.0646 10.7475 73.1499 10.8328C73.2352 10.9181 73.2779 11.0355 73.2779 11.1848V32.6248C73.2779 32.7741 73.2352 32.8915 73.1499 32.9768C73.0646 33.0621 72.9472 33.1048 72.7979 33.1048H67.7419Z"
                                    fill="var(--p-primary-color)"
                                />
                                <path
                                    d="M57.2902 33.3608C55.2635 33.3608 53.5462 32.8168 52.1382 31.7288C50.7515 30.6408 49.8342 29.1688 49.3862 27.3128C49.1728 26.5448 49.0662 25.6915 49.0662 24.7528C49.0662 23.7075 49.1942 22.7581 49.4502 21.9048C49.9622 20.1341 50.9008 18.7475 52.2662 17.7448C53.6528 16.7208 55.3382 16.2088 57.3222 16.2088C59.3062 16.2088 60.9702 16.7208 62.3142 17.7448C63.6795 18.7475 64.6182 20.1128 65.1302 21.8408C65.3862 22.7368 65.5142 23.6861 65.5142 24.6888C65.5142 25.4995 65.4288 26.3101 65.2582 27.1208C64.8102 29.0408 63.8822 30.5661 62.4742 31.6968C61.0875 32.8061 59.3595 33.3608 57.2902 33.3608ZM57.2902 28.2088C57.8448 28.2088 58.2928 28.0275 58.6342 27.6648C58.9755 27.2808 59.2102 26.7795 59.3382 26.1608C59.4235 25.7555 59.4662 25.2755 59.4662 24.7208C59.4662 24.2301 59.4128 23.7395 59.3062 23.2488C58.9862 21.9901 58.3142 21.3608 57.2902 21.3608C56.2235 21.3608 55.5515 21.9901 55.2742 23.2488C55.1675 23.6115 55.1142 24.1021 55.1142 24.7208C55.1142 25.2755 55.1568 25.7555 55.2422 26.1608C55.5622 27.5261 56.2448 28.2088 57.2902 28.2088Z"
                                    fill="var(--p-primary-color)"
                                />
                                <path
                                    d="M37.5712 33.1048C37.4432 33.1048 37.3258 33.0728 37.2192 33.0088C37.1125 32.9235 37.0485 32.8168 37.0272 32.6888L30.7232 11.2488C30.7018 11.2061 30.6912 11.1528 30.6912 11.0888C30.6912 10.8328 30.8405 10.7048 31.1392 10.7048H36.6112C36.8885 10.7048 37.0592 10.8435 37.1232 11.1208L40.3232 24.6248C40.3445 24.7101 40.3765 24.7528 40.4192 24.7528C40.4618 24.7528 40.4938 24.7101 40.5152 24.6248L43.6192 11.1208C43.6832 10.8435 43.8538 10.7048 44.1312 10.7048H49.4752C49.6458 10.7048 49.7632 10.7581 49.8272 10.8648C49.9125 10.9501 49.9338 11.0781 49.8912 11.2488L43.5232 32.6888C43.5018 32.8168 43.4378 32.9235 43.3312 33.0088C43.2245 33.0728 43.1072 33.1048 42.9792 33.1048H37.5712Z"
                                    fill="var(--p-primary-color)"
                                />
                                <path
                                    fill-rule="evenodd"
                                    clip-rule="evenodd"
                                    d="M4.043 15.0334L8.03101 16.6142H10.7377L11.713 0.106103C11.7195 -0.00249146 11.5724 -0.0417968 11.5238 0.0555237L4.043 15.0334ZM2.55847 23.2515H0.100129C0.0258101 23.2515 -0.0225409 23.1733 0.0106666 23.1068L2.30586 18.5114L4.69286 17.9483L2.55847 21.1927V23.2515ZM17.4689 29.2273L10.9293 39.2178C10.8699 39.3085 10.7288 39.2531 10.747 39.1462L13.4481 23.2515H4.44864V21.8287H4.46887L6.90673 17.9375L8.42408 18.9076H13.5137L15.031 17.9375L17.4689 21.8287V29.2273ZM20.0244 17.8162H24.7534C24.8329 17.8162 24.8806 17.9044 24.8371 17.9709L19.3793 26.3088V21.1927L17.2449 17.9483L19.3793 18.595L20.0244 17.8162Z"
                                    fill="var(--p-primary-color)"
                                />
                            </svg>
                        </span>
                        <span>
                            <Button type="button" @click="closeCallback" icon="pi pi-times" rounded outlined></Button>
                        </span>
                    </div>
                    <div class="overflow-y-auto">
                        <ul class="list-none p-4 m-0">
                            <li>
                                <div
                                    v-styleclass="{
                                        selector: '@next',
                                        enterFromClass: 'hidden',
                                        enterActiveClass: 'animate-slidedown',
                                        leaveToClass: 'hidden',
                                        leaveActiveClass: 'animate-slideup'
                                    }"
                                    class="p-4 flex items-center justify-between text-surface-500 dark:text-surface-400 cursor-pointer"
                                >
                                    <span class="font-medium">FAVORITES</span>
                                    <i class="pi pi-chevron-down"></i>
                                </div>
                                <ul class="list-none p-0 m-0 overflow-hidden">
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-home mr-2"></i>
                                            <span class="font-medium">Dashboard</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-bookmark mr-2"></i>
                                            <span class="font-medium">Bookmarks</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a
                                            v-styleclass="{
                                                selector: '@next',
                                                enterFromClass: 'hidden',
                                                enterActiveClass: 'animate-slidedown',
                                                leaveToClass: 'hidden',
                                                leaveActiveClass: 'animate-slideup'
                                            }"
                                            class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors"
                                        >
                                            <i class="pi pi-chart-line mr-2"></i>
                                            <span class="font-medium">Reports</span>
                                            <i class="pi pi-chevron-down ml-auto"></i>
                                        </a>
                                        <ul class="list-none py-0 pl-4 pr-0 m-0 hidden overflow-y-hidden transition-all duration-[400ms] ease-in-out">
                                            <li>
                                                <a
                                                    v-styleclass="{
                                                        selector: '@next',
                                                        enterFromClass: 'hidden',
                                                        enterActiveClass: 'animate-slidedown',
                                                        leaveToClass: 'hidden',
                                                        leaveActiveClass: 'animate-slideup'
                                                    }"
                                                    class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors"
                                                >
                                                    <i class="pi pi-chart-line mr-2"></i>
                                                    <span class="font-medium">Revenue</span>
                                                    <i class="pi pi-chevron-down ml-auto"></i>
                                                </a>
                                                <ul class="list-none py-0 pl-4 pr-0 m-0 hidden overflow-y-hidden transition-all duration-[400ms] ease-in-out">
                                                    <li>
                                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                                            <i class="pi pi-table mr-2"></i>
                                                            <span class="font-medium">View</span>
                                                        </a>
                                                    </li>
                                                    <li>
                                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                                            <i class="pi pi-search mr-2"></i>
                                                            <span class="font-medium">Search</span>
                                                        </a>
                                                    </li>
                                                </ul>
                                            </li>
                                            <li>
                                                <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                                    <i class="pi pi-chart-line mr-2"></i>
                                                    <span class="font-medium">Expenses</span>
                                                </a>
                                            </li>
                                        </ul>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-users mr-2"></i>
                                            <span class="font-medium">Team</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-comments mr-2"></i>
                                            <span class="font-medium">Messages</span>
                                            <span class="inline-flex items-center justify-center ml-auto bg-primary text-primary-contrast rounded-full" style="min-width: 1.5rem; height: 1.5rem">3</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-calendar mr-2"></i>
                                            <span class="font-medium">Calendar</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-cog mr-2"></i>
                                            <span class="font-medium">Settings</span>
                                        </a>
                                    </li>
                                </ul>
                            </li>
                        </ul>
                        <ul class="list-none p-4 m-0">
                            <li>
                                <div
                                    v-styleclass="{
                                        selector: '@next',
                                        enterFromClass: 'hidden',
                                        enterActiveClass: 'animate-slidedown',
                                        leaveToClass: 'hidden',
                                        leaveActiveClass: 'animate-slideup'
                                    }"
                                    class="p-4 flex items-center justify-between text-surface-500 dark:text-surface-400 cursor-pointer"
                                >
                                    <span class="font-medium">APPLICATION</span>
                                    <i class="pi pi-chevron-down"></i>
                                </div>
                                <ul class="list-none p-0 m-0 overflow-hidden">
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-folder mr-2"></i>
                                            <span class="font-medium">Projects</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-chart-bar mr-2"></i>
                                            <span class="font-medium">Performance</span>
                                        </a>
                                    </li>
                                    <li>
                                        <a class="flex items-center cursor-pointer p-4 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                                            <i class="pi pi-cog mr-2"></i>
                                            <span class="font-medium">Settings</span>
                                        </a>
                                    </li>
                                </ul>
                            </li>
                        </ul>
                    </div>
                    <div class="mt-auto">
                        <hr class="mb-4 mx-4 border-t border-0 border-surface-200 dark:border-surface-700" />
                        <a class="m-4 flex items-center cursor-pointer p-4 gap-2 rounded text-surface-700 hover:bg-surface-100 dark:text-surface-0 dark:hover:bg-surface-800 duration-150 transition-colors">
                            <Avatar image="https://primefaces.org/cdn/primevue/images/avatar/amyelsner.png" shape="circle" />
                            <span class="font-bold">Amy Elsner</span>
                        </a>
                    </div>
                </div>
            </template>
        </Drawer>
        <Button icon="pi pi-bars" @click="visible = true" />
    </div>
</template>

<script setup lang="ts">
import Avatar from '@/volt/Avatar.vue';
import Button from '@/volt/Button.vue';
import Drawer from '@/volt/Drawer.vue';
import { ref } from 'vue';

const visible = ref(false);
<\/script>
`);
</script>
