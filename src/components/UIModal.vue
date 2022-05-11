<template>
    <div v-if="showed" class="modal modal-component">
        <div class="modal-background" @click='onClose'/>
        <div class="modal-card">
            <slot/>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        value: {
            type: Boolean,
            required: true,
        },
    },
    computed: {
        showed: {
            get() {
                return this.value
            },
            set(isShowed) {
                this.$emit('input', isShowed)
            },
        },
    },
    methods: {
        onClose() {
            this.$emit('closed')
        }
    }
}
</script>