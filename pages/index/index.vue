<template>
	<u-swiper :list="list1" @change="change" @click="click"></u-swiper>
</template>

<script>
export default {
	data() {
		return {
			list1: ['https://cdn.uviewui.com/uview/swiper/swiper1.png', 'https://cdn.uviewui.com/uview/swiper/swiper2.png', 'https://cdn.uviewui.com/uview/swiper/swiper3.png'],
			show: true
		};
	}
};
</script>
