<template>
  <div class="w-full md:w-1/2">
		<div
			class="leading-loose max-w-xl m-4 p-7 bg-secondary-light dark:bg-secondary-dark rounded-xl shadow-xl text-left"
		>
			<p
				class="font-general-medium text-primary-dark dark:text-primary-light text-2xl mb-8"
			>
				Contact Form
			</p>
			<form @submit.prevent="sendEmail" class="font-general-regular space-y-7">
				<FormInput label="Full Name" v-model="name" inputIdentifier="name" />
				<FormInput
					label="Email"
					inputIdentifier="email"
					inputType="email"
					v-model="email"
				/>
				<FormInput label="Subject"  v-model="subject" inputIdentifier="subject" />
				<FormTextarea label="Message" v-model="message" textareaIdentifier="message" />

				<div>
					<Button
						title="Send Message"
						class="px-4 py-2.5 text-white tracking-wider bg-indigo-500 hover:bg-indigo-600 focus:ring-1 focus:ring-indigo-900 rounded-lg duration-500"
						type="submit"
						aria-label="Send Message"
					/>
				</div>
			</form>
		</div>
	</div>
</template>

<script>
import emailjs from 'emailjs-com';
import Button from '../reusable/ButtonUI.vue';
import FormInput from '../reusable/FormInput.vue';
import FormTextarea from '../reusable/FormTextarea.vue';
export default {
	data(){
		return {
		name: '',
		email : '',
		subject: '',
		message : '',
		}
	},
	methods: {
		sendEmail(e){
			try{
				emailjs.sendForm("service_io2bqqf", "template_pe40ogh", e.target, "mg07CKtspvkEaZqSD",{
					name: this.name,
					email : this.email,
					subject : this.subject,
					message: this.message,
				});
			}catch(err){
			console.log({err});
		}
		this.name= '';
		this.email= '';
		this.subject= '';
		this.message= '';
		
	},
	},
    components: { 
        Button, FormInput, FormTextarea 
        } 
    };
</script>

<style>

</style>