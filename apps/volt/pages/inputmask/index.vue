<template>
    <DocComponent title="Vue Mask Component" header="InputMask" description="InputMask component is used to enter input in a certain format such as numeric, date, currency, email and phone." :componentDocs="docs" />
</template>

<script setup lang="ts">
import BasicDoc from '@/doc/inputmask/BasicDoc.vue';
import DisabledDoc from '@/doc/inputmask/DisabledDoc.vue';
import DownloadDoc from '@/doc/inputmask/DownloadDoc.vue';
import FilledDoc from '@/doc/inputmask/FilledDoc.vue';
import ImportDoc from '@/doc/inputmask/ImportDoc.vue';
import InvalidDoc from '@/doc/inputmask/InvalidDoc.vue';
import MaskDoc from '@/doc/inputmask/MaskDoc.vue';
import OptionalDoc from '@/doc/inputmask/OptionalDoc.vue';
import SizesDoc from '@/doc/inputmask/SizesDoc.vue';
import SlotCharDoc from '@/doc/inputmask/SlotCharDoc.vue';
import { ref } from 'vue';

const docs = ref([
    {
        id: 'dowload',
        label: 'Download',
        component: DownloadDoc
    },
    {
        id: 'import',
        label: 'Import',
        component: ImportDoc
    },
    {
        id: 'basic',
        label: 'Basic',
        component: BasicDoc
    },
    {
        id: 'mask',
        label: 'Mask',
        component: MaskDoc
    },
    {
        id: 'optional',
        label: 'Optional',
        component: OptionalDoc
    },
    {
        id: 'slotchar',
        label: 'SlotChar',
        component: SlotCharDoc
    },
    {
        id: 'filled',
        label: 'Filled',
        component: FilledDoc
    },
    {
        id: 'sizes',
        label: 'Sizes',
        component: SizesDoc
    },
    {
        id: 'invalid',
        label: 'Invalid',
        component: InvalidDoc
    },
    {
        id: 'disabled',
        label: 'Disabled',
        component: DisabledDoc
    }
]);
</script>
