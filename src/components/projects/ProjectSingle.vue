<script>
export default {
	props: ['project'],
};
</script>

<template>
	<a :href="project.link">
		<div>
			<img
				:src="project.img"
				:alt="project.title"
				:width="project.width"
				class="rounded-t-xl border-none"
			/>
		</div>
		<div class="text-center px-4 py-6">
			<p
				class="font-general-semibold text-xl text-ternary-dark dark:text-ternary-light font-semibold mb-2"
			>
				{{ project.title }}
			</p>
			<span
				class="font-general-medium text-lg text-ternary-dark dark:text-ternary-light"
				>{{ project.category }}</span
			>
		</div>
	</a>
</template>

<style lang="scss" scoped></style>
