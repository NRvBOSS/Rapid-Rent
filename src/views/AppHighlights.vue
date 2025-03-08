<template>
  <div class="flex justify-between ">
    <p class="mx-25 my-10 font-bold text-2xl w-30">Highlights</p>
    <a class="mx-25 my-10 cursor-pointer group relative"
      >View more&rarr;
      <div
        class="bg-black h-[2px] w-full scale-x-0 origin-center group-hover:scale-x-100 transition-transform duration-500"
      ></div>
    </a>
  </div>

  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 px-8">
    <div
      v-for="(car, index) in cars"
      :key="index"
      class="bg-[#f4f4f4] rounded-2xl shadow-lg p-6"
    >
      <img
        class="w-full h-48 object-cover rounded-t-2xl"
        src="../photos/710_n_84bQNwZvpGSEPPCvJ-ng.jpg"
        :alt="car.name"
      />

      <div class="grid grid-cols-2 gap-4 text-gra-700 mt-4">
        <p class="font-semibold">{{ car.name }}</p>
        <p class="col-span-2">{{ car.year }}</p>
        <p>🚗 {{ car.people }} People</p>
        <p>⛽ {{ car.fuel }}</p>
        <p>⚙️ {{ car.transmission }}</p>
        <p>⛽ {{ car.fuelConsumption }}</p>
      </div>

      <div class="flex justify-between items-center mt-6">
        <p class="text-xl font-bold text-gray-900">${{ car.price }}/month</p>
        <button
          class="bg-blue-600 text-white py-2 px-5 rounded-lg shadow-md hover:bg-blue-700 transition duration-300"
        >
          Rent now
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cars: [
        {
          name: "Toyota Land Cruiser",
          year: 2018,
          people: 4,
          fuel: "Oil",
          transmission: "Automatic",
          fuelConsumption: "6.1km/1-litre",
          price: 440,
        //   const image = img: "../photos/710_n_84bQNwZvpGSEPPCvJ-ng.jpg",
        },
      ],
    };
  },
};
</script>
