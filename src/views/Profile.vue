<template>
  <div class="flex flex-col items-center">
    <div class="max-w-md mx-auto">
      <div class="bg-white shadow-md rounded-lg overflow-hidden">
        <img class="w-full h-64 object-cover object-center" :src="$auth.user.picture" alt="Perfil">
        <div class="p-6">
          <h2 class="text-xl font-semibold mb-2">{{ $auth.user.name }}</h2>
          <p class="text-gray-600 mb-2">{{ $auth.user.email }}</p>
          <div class="border-b border-gray-200 mb-4"></div>
          <p class="text-gray-600"><span class="font-semibold">Nickname:</span> {{ $auth.user.nickname }}</p>
          <p class="text-gray-600"><span class="font-semibold">Localización:</span> {{ $auth.user.locale }}</p>
          <p class="text-gray-600"><span class="font-semibold">Última actualización:</span> {{ $auth.user.updated_at }}</p>
          <p class="text-gray-600"><span class="font-semibold">Correo electrónico verificado:</span> {{ $auth.user.email_verified ? 'Sí' : 'No' }}</p>
          <p class="text-gray-600"><span class="font-semibold">Sub:</span> {{ $auth.user.sub }}</p>
        </div>
      </div>
    </div>

    <div class="max-w-md mx-auto mt-8">
      <div class="bg-white rounded-lg overflow-hidden shadow-md hover:shadow-lg transition duration-300">
        <div class="p-6">
          <pre class="text-sm">{{ JSON.stringify($auth.user, null, 2) }}</pre>
        </div>
      </div>
    </div>
  </div>
</template>
