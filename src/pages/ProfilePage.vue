<template>
  <div class="min-h-screen bg-gray-100 flex items-center justify-center p-6">
    <div class="bg-white shadow-xl rounded-3xl p-10 w-full max-w-3xl">

      <!-- PROFILE HEADER -->
      <div class="text-center">
        <img
          src="/profile.jpg"
          class="w-32 h-32 rounded-full mx-auto shadow-md object-cover"
          alt="profile"
        />

        <h1 class="text-3xl font-bold mt-4 text-gray-800">{{ profile.name }}</h1>
        <p class="text-lg text-gray-500 mt-1">{{ profile.position }}</p>
      </div>

      <!-- ABOUT -->
      <div class="mt-8">
        <h2 class="text-xl font-semibold text-gray-800">About Me</h2>
        <p class="text-gray-600 mt-2 leading-relaxed">
          {{ profile.about }}
        </p>
      </div>

      <!-- SKILLS -->
      <div class="mt-8">
        <h2 class="text-xl font-semibold text-gray-800">Skills</h2>
        <div class="flex flex-wrap gap-2 mt-3">
          <span
            v-for="skill in profile.skills"
            :key="skill"
            class="px-4 py-1 bg-blue-100 text-blue-700 rounded-full text-sm font-medium"
          >
            {{ skill }}
          </span>
        </div>
      </div>

      <!-- LINKS -->
      <div class="mt-8">
        <h2 class="text-xl font-semibold text-gray-800">Links</h2>

        <div class="flex gap-4 mt-4">
          <a
            v-for="link in profile.links"
            :key="link.label"
            :href="link.url"
            target="_blank"
            class="px-4 py-2 rounded-lg bg-gray-800 text-white hover:bg-gray-900"
          >
            {{ link.label }}
          </a>
        </div>
      </div>

    </div>
  </div>
</template>

<script setup>
const profile = {
  name: "Ping Pony",
  position: "Backend Engineer | Golang | Microservices",
  about:
    "I'm passionate about backend development, distributed systems, microservices, and cloud-native architectures. I love building scalable systems with Go and gRPC.",
  skills: [
    "Golang",
    "GRPC",
    "REST API",
    "Microservices",
    "Docker",
    "Kubernetes",
    "PostgreSQL",
    "Gin",
    "Vue.js",
    "Redis"
  ],
  links: [
    { label: "GitHub", url: "https://github.com/yourgithub" },
    { label: "LinkedIn", url: "https://linkedin.com/in/yourprofile" },
    { label: "Email", url: "mailto:your@email.com" }
  ]
};
</script>

<style scoped>
</style>
