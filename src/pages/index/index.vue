<template>
    <view class="page-index">
        <nut-button type="primary" @tap="onClick">按钮</nut-button>
        <nut-toast v-model:visible="show" msg="123" />
        <view>{{ appId }}</view>
        <view>{{ apiBaseUrl }}</view>
    </view>
</template>

<script setup>
    import './index.scss'

    const show = ref(false)
    const onClick = () => {
        show.value = true
        // showToast('你点击了')
    }

    const appId = ref(process.env.APP_ID)
    const apiBaseUrl = ref(process.env.API_BASE_URL)
</script>
