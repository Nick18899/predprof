<template>
    <div class="block">
        <el-date-picker
                :picker-options="pickerOptions"
                align="right"
                end-placeholder="End date"
                range-separator="To"
                start-placeholder="Start date"
                type="datetimerange"
                @input="$emit('model:update', $event.target.value)">
        </el-date-picker>
    </div>
</template>

<script>
    export default {
        name: "DatePicker",
        data() {
            return {
                pickerOptions: {
                    shortcuts: [{
                        text: 'Last week',
                        onClick(picker) {
                            const end = new Date();
                            const start = new Date();
                            start.setTime(start.getTime() - 3600 * 1000 * 24 * 7);
                            picker.$emit('pick', [start, end]);
                        }
                    }, {
                        text: 'Last month',
                        onClick(picker) {
                            const end = new Date();
                            const start = new Date();
                            start.setTime(start.getTime() - 3600 * 1000 * 24 * 30);
                            picker.$emit('pick', [start, end]);
                        }
                    }, {
                        text: 'Last 3 months',
                        onClick(picker) {
                            const end = new Date();
                            const start = new Date();
                            start.setTime(start.getTime() - 3600 * 1000 * 24 * 90);
                            picker.$emit('pick', [start, end]);
                        }
                    }]
                },
                value2: ''
            };
        }
    }
</script>

<style scoped>

</style>
