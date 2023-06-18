<template>
	<div>
		<h1>{{ $t("hello", { name: "vue-i18n" }) }}</h1>
		<p>{{ $t("description") }}</p>
		<form>
			<label for="locale-select">{{ $t("language") }}: </label>
			<select
				id="locale-select"
				v-model="$i18n.locale">
				<option
					v-for="(locale, index) in $i18n.availableLocales"
					:key="index"
					:value="locale">
					{{ locale }}
				</option>
			</select>
		</form>
	</div>
</template>
