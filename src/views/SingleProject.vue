<template>
  <div class="container mx-auto mt-10 sm:mt-20">
		<!-- Project header -->
		<ProjectHeader :singleProjectHeader="singleProjectHeader" />

		<!-- Project gallery -->
		<ProjectGallery :projectImages="projectImages" />

		<!-- Project information -->
		<ProjectInfo :projectInfo="projectInfo" />

		<!-- Project related projects -->
		<ProjectRelatedProjects :relatedProject="relatedProject" />
	</div>
</template>

<script>
import feather from 'feather-icons';
import ProjectHeader from '../components/projects/ProjectHeader.vue';
import ProjectGallery from '../components/projects/ProjectGallery.vue';
import ProjectInfo from '../components/projects/ProjectInfo.vue';
import ProjectRelatedProjects from '../components/projects/ProjectRelatedProjects.vue';
export default {
	name: 'Projects',
	components: {
		ProjectHeader,
		ProjectGallery,
		ProjectInfo,
		ProjectRelatedProjects,
	},
	data: () => {
		return {
			singleProjectHeader: {
				singleProjectTitle: 'Bachelor Project',
				singleProjectDate: 'Dec 17, 2022',
				singleProjectTag: 'Full-Stack Web Developer',
			},
			projectImages: [
				{
					id: 1,
					title: 'Login',
					img: require('@/assets/images/BPR2.png'),
				},
				{
					id: 2,
					title: 'Profile',
					img: require('@/assets/images/bpr3.png'),
				},
				{
					id: 3,
					title: 'Chat',
					img: require('@/assets/images/test.png'),
				},
			],
			projectInfo: {
				clientHeading: '',
				companyInfos: [
				],
				objectivesHeading: 'Objective',
				objectivesDetails: '',
				technologies: [
					{
						title: 'Tools & Technologies',
						techs: [
							'HTML',
							'CSS',
							'C#',
							'.NET',
							'SQL',
							'Microsoft Azure',
						],
					},
				],
				projectDetailsHeading: 'Challenge',
				projectDetails: [
					{
						id: 1,
						details:
					'This project aims to create an application that students can use to communicate with each other, with the aim to build a community of software engineers’ students, allowing them to chat with each other, make posts for announcements, seeking for help, sharing ideas. The application uses Microsoft Azure as a cloud provider. To establish the connection between each part of the project, Microsoft Azure, SQLite, REST and HTTP requests were used. Implementation of all the system is built with .NET both for the front-end and the server. This project fulfils all the requirements set on the analysis and can be accessible through the cloud using Azure Cloud Services.',
					},
					{
						id: 2,
						details:
							'Social media is and always have been an important source of entertainment, and a way to connect people all around the world. According to research on social media, the global consumers that use social media the most are between 20-29 years old. Most inside that range of age are students enrolled in some type of education. But for students enrolled in VIA University College there is not a social media focused on them. Students have tools to aid them see the calendar or information for the class like ItsLearning, but there is not such a tool to communicate with each other to build a community of students. ',
					},
					{
						id: 3,
						details:
							'For these reasons, our group decided to make a social media for students, specifically Software Engineering students, to offer them a space where they could build a community by communicating with each other, offering for help, and share their ideas.',
					},
				],
				socialSharingsHeading: 'Share This',
				socialSharings: [
					{
						id: 1,
						name: 'Twitter',
						icon: 'twitter',
						url: 'https://twitter.com/',
					},
					{
						id: 2,
						name: 'Instagram',
						icon: 'instagram',
						url: 'https://instagram.com/',
					},
					{
						id: 3,
						name: 'Facebook',
						icon: 'facebook',
						url: 'https://facebook.com/',
					},
					{
						id: 4,
						name: 'LinkedIn',
						icon: 'linkedin',
						url: 'https://linkedin.com/',
					},
					{
						id: 5,
						name: 'Youtube',
						icon: 'youtube',
						url: 'https://www.youtube.com/',
					},
				],
			},
			relatedProject: {
				relatedProjectsHeading: 'Related Projects',
				relatedProjects: [
					{
						id: 1,
						title: 'Mobile UI',
						img: require('@/assets/images/mobile-project-1.jpg'),
					},
					{
						id: 2,
						title: 'Web Application',
						img: require('@/assets/images/web-project-1.jpg'),
					},
					{
						id: 3,
						title: 'UI Design',
						img: require('@/assets/images/ui-project-2.jpg'),
					},
					{
						id: 4,
						title: 'Kabul Mobile App UI',
						img: require('@/assets/images/mobile-project-2.jpg'),
					},
				],
			},
		};
	},
	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
	methods: {},
};
</script>
<style scoped></style>