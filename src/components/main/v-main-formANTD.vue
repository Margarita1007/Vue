<template>
    <div class="form-container">
        <a-form
        :model="formState"
        name="basic"
        layout="vertical"
        
        autocomplete="off"
        @finish="onFinish"
        @finishFailed="onFinishFailed"
        >
            <a-form-item
                label = "Адрес страницы"
                name = "address"
            >
                <a-input v-model:value="formState.address" placeholder="Вставьте сюда ссылку" />
            </a-form-item>

            <a-form-item label="Источник трафика">
                <a-radio-group v-model:value="formState.traffic">
                    <a-radio value="1">Свои значения</a-radio>
                    <a-radio value="2">Google Adword</a-radio>
                    <a-radio value="3">Яндекс.Директ</a-radio>
                    <a-radio value="4">Вконтакте</a-radio>
                    <a-radio value="5">Facebook</a-radio>
                    <a-radio value="6">Target My.com</a-radio>
                </a-radio-group>
            </a-form-item>
        </a-form>
        <div class="form-result">
            <a-row>
                <a-col span="24">Результат</a-col>
                <a-col>
                    <a-input v-model:value="formState.resultRef" readonly/>
                </a-col>
            </a-row>

        </div>
    </div>
    
  </template>

<script>


import { computed } from '@vue/reactivity';
import { defineComponent, reactive } from 'vue';

export default defineComponent({
  setup() {
    const formState = reactive({
      address: '',
      traffic: '1',
      remember: true,
      resultRef: computed(() => formState.address ? formState.address + '/?' : '')
    });

    
    const onFinish = (values) => {
      console.log('Success:', values);
    };

    const onFinishFailed = (errorInfo) => {
      console.log('Failed:', errorInfo);
    };
    return {
      formState,
      onFinish,
      onFinishFailed,
    };
  },
});
</script>

<style>
.form-container {
    max-width: 1236px;
    padding: 24px 0;
    margin: auto;
}

.ant-form-item-label > label {
    font-weight: 600;
    font-size: 16px !important;
    line-height: 24px !important;
    color: #303446 !important;
}

.ant-radio-group {
    display: flex !important;
    justify-content: flex-start;
    flex-wrap: wrap;
}

.ant-radio-wrapper {
    margin-right: 24px !important;
}

.ant-radio-checked .ant-radio-inner{
  border: none !important;
  background: #FFB6B6 !important;
}

.ant-radio-checked .ant-radio-inner:after{
  background-color: #ED5252;
}

.ant-radio-checked .ant-radio-inner,
.ant-radio:hover .ant-radio-inner,
.ant-radio-wrapper:hover,
.ant-radio-input:focus .ant-radio-inner,
.ant-radio-wrapper:focus
 {
  border-color: red !important;
}

</style>