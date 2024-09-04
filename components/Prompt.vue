<template>
    <div class="flex flex-col items-center justify-center p-4 bg-gray-100 rounded-lg shadow-lg">
        <input type="text" v-model="promptMessage"
            class="w-full p-2 mb-4 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
            placeholder="Enter your prompt message here" />
        <button @click="generateOutput" class="px-4 py-2 text-white bg-blue-500 rounded-md hover:bg-blue-600">
            Generate Response
        </button>
        <div v-if="output" class="mt-4 text-lg font-semibold text-gray-800">
           {{ output }}
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            promptMessage: "", // Holds the prompt message input by the user
            output: null,      // Holds the output returned from the prompt
        };
    },
    methods: {
        async generateOutput() {
            try {
                const canCreate = await window.ai.canCreateTextSession();
                if (canCreate !== "no") {
                    const session = await window.ai.createTextSession();
                    console.log(session)
                    this.output = await session.prompt(this.promptMessage);
                    
                } else {
                    console.log('Cannot create')
                }
            } catch (error) {
                console.error(error)
            }
        },
    },
};
</script>

<style scoped>
/* Add custom styles if needed */
</style>
