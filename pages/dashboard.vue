<template>
	<div>Dashboard</div>
	<button @click="logOutUser">Sign out</button>
</template>

<script setup lang="ts">
	definePageMeta({ middleware: "auth" });

	const { signOut } = useAuth();

	const logOutUser = async () => {
		await signOut({ callbackUrl: "/" });
	};
</script>

<style scoped></style>
