<template>
    <DocSectionText v-bind="$attrs">
        <p>
            PrimeVue uses the <i>system</i> as the default <i>darkModeSelector</i> in theme configuration. If you have a dark mode switch in your application, set the <i>darkModeSelector</i> to the selector you utilize such as <i>.my-app-dark</i> so
            that PrimeVue can fit in seamlessly with your color scheme.
        </p>
        <DocSectionCode :code="code1" hideToggleCode importCode hideStackBlitz />
        <p>
            Following is a very basic example implementation of a dark mode switch, you may extend it further by involving <i>prefers-color-scheme</i> to retrieve it from the system initially and use <i>localStorage</i> to make it stateful. See this
            <a href="https://dev.to/abbeyperini/dark-mode-toggle-and-prefers-color-scheme-4f3m" target="_blank" rel="noopener noreferrer">article</a> for more information.
        </p>
        <DocSectionCode :code="code2" hideToggleCode hideStackBlitz />
        <DocSectionCode :code="code3" hideToggleCode importCode hideStackBlitz />
        <p>In case you prefer to use dark mode all the time, apply the <i>darkModeSelector</i> initially and never change it.</p>
        <DocSectionCode :code="code4" hideToggleCode hideStackBlitz />
        <p>It is also possible to disable dark mode completely using <i>false</i> or <i>none</i> as the value of the selector.</p>
        <DocSectionCode :code="code5" hideToggleCode importCode hideStackBlitz />
    </DocSectionText>
</template>

<script>
export default {
    data() {
        return {
            code1: {
                basic: `
import PrimeVue from 'primevue/config';
import Aura from '@primeuix/themes/aura';

const app = createApp(App);

app.use(PrimeVue, {
    // Default theme configuration
    theme: {
        preset: Aura,
        options: {
            darkModeSelector: '.my-app-dark',
        }
    }
 });
`
            },
            code2: {
                basic: `
<Button label="Toggle Dark Mode" @click="toggleDarkMode()" />
`
            },
            code3: {
                basic: `
function toggleDarkMode() {
    document.documentElement.classList.toggle('my-app-dark');
}
`
            },
            code4: {
                basic: `
<html class="my-app-dark">
`
            },
            code5: {
                basic: `
theme: {
    preset: Aura,
    options: {
        darkModeSelector: false || 'none',
    }
}
`
            }
        };
    }
};
</script>
