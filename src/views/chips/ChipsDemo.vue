<template>
    <div>
        <div class="content-section introduction">
            <div class="feature-intro">
                <h1>Chips</h1>
                <p>Chips is used to enter multiple values on an input field.</p>
            </div>
        </div>

        <div class="content-section implementation p-fluid">
            <h3 class="first">Basic</h3>
            <Chips v-model="value1" />

            <h3>Comma Separator</h3>
            <Chips v-model="value2" separator="," />

            <h3>Template</h3>
            <Chips v-model="value3">
                <template #chip="slotProps">
                    <div>
                        <span>{{slotProps.value}} - (active) </span>
                        <i class="pi pi-user-plus" style="font-size: 14px"></i>
                    </div>
                </template>
            </Chips>
        </div>

        <ChipsDoc />
    </div>
</template>

<script>
import ChipsDoc from './ChipsDoc';

export default {
    data() {
        return {
            value1: null,
            value2: null,
            value3: null
        }
    },
    components: {
        'ChipsDoc': ChipsDoc
    }
}
</script>
