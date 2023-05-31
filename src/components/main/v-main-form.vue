<template>
    <form class="form1">
        <div class="row row1">
            <h3>Адрес страницы</h3>
            <label>
                <input type="text" placeholder="Вставьте сюда свою ссылку" v-model="utm.address"/>
            </label>
        </div>
        <div class="row row2">
            <h3>Источник трафика</h3>
            <div class="row2-radio-group">
                <div>
                    <input type="radio" value="1" v-model="utm.traffic">
                    <label for="1">Свои значения</label>
                </div>
                <div>
                    <input type="radio" value="2" v-model="utm.traffic">
                    <label for="2">Google adwords</label>
                </div>
                <div>
                    <input type="radio" value="3" v-model="utm.traffic">
                    <label>Яндекс.Директ</label>
                </div>
                <div>
                    <input type="radio" value="4" v-model="utm.traffic">
                    <label>Вконтакте</label>
                </div>
                <div>
                    <input type="radio" value="5" v-model="utm.traffic">
                    <label>Facebook</label>
                </div>
                <div>
                    <input type="radio" value="6" v-model="utm.traffic">
                    <label>Target My.com</label>
                </div>
            </div>
            
        </div>
        <div class="parameters-container">
            <div class="parameters-group row">
                <h3>Обязательные параметры</h3>
                <div class="parameters required-parameters">
                    <div class="param">
                        <h4>Источник кампании</h4>
                        <div class="utm-parameter">
                            <div class="utm-parameter-label">
                                <span>utm_source</span>
                                <span>!</span>
                            </div>
                            <label class="utm-parameter-input">
                                <input type="text" placeholder="google, yandex, vk, facebook" v-model="utm.utm_source">
                            </label>
                        </div>
                    </div>
                    <div>
                        <h4>Тип трафика</h4>
                        <div class="utm-parameter">
                            <div class="utm-parameter-label">
                                <span>utm_medium</span>
                                <span>!</span>
                            </div>
                            <label class="utm-parameter-input">
                                <input type="text" placeholder="cpc, email, banner, article" v-model="utm.utm_medium">
                            </label>
                        </div>
                    </div>
                    <div>
                        <h4>Название кампании</h4>
                        <div class="utm-parameter">
                            <div class="utm-parameter-label">
                                <span>utm_campaign</span>
                                <span>!</span>
                            </div>
                            <label class="utm-parameter-input">
                                <input type="text" placeholder="promo, discount, sale" v-model="utm.utm_campaign">
                            </label>
                        </div>
                    </div>

                </div>
            </div>


            <div class="parameters-group row">
                <h3>Необязательные параметры</h3>
                <div class="parameters optional-parameters">
                    <div class="param">
                        <h4>Идентификатор объявления</h4>
                        <div class="utm-parameter">
                            <div class="utm-parameter-label">
                                <span>utm_content</span>
                                <span>!</span>
                            </div>
                            <label class="utm-parameter-input">
                                <input type="text" placeholder="link, landing" v-model="utm.utm_content">
                            </label>
                        </div>
                    </div>
                    <div>
                        <h4>Ключевое слово</h4>
                        <div class="utm-parameter">
                            <div class="utm-parameter-label">
                                <span>utm_term</span>
                                <span>!</span>
                            </div>
                            <label class="utm-parameter-input">
                                <input type="text" placeholder="registration, loan" v-model="utm.utm_term">
                            </label>
                        </div>
                    </div>

                    <!-- <div>
                        <h3>Результат</h3>
                        <label>
                            <input type="text" placeholder="Здесь появится UTM метка" readonly v-model="resultRef">
                        </label>
                    </div> -->

                </div>
            </div>
        </div>
    </form>
</template>

<script>
export default {
    name: "v-main-form",
    data() {
        return {
            utm: {
                address: '',
                traffic: '',
                utm_source: '',
                utm_medium: '',
                utm_campaign: '',
                utm_content: '',
                utm_term: '' 
            }
        }
    },
    computed: {
        resultRef() {
            const ref = [];
            for (var key in this.utm) {
                ref.push({key: this.utm[key]})
            }
            return ref
        }
    }
}
</script>

<style>
.form1 {
    display: flex;
    flex-direction: column;
    gap: 24px;
}

.form1 .row {
    display: flex;
    flex-direction: column;
    gap: 8px;
    text-align: left;
}

.form1 .row h3 {
    margin: 0;
    font-size: 16px;
    line-height: 24px;
    color: #303446;
    font-weight: 600;
}

.row2-radio-group {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    width: 100%;
}

.row2-radio-group div {
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-right: 24px;
    gap: 12px;
}

.parameters-container {
    display: flex;
    flex-direction: row;
    gap: 46px;
}

.parameters {
    display: flex;
    flex-direction: column;
    gap: 23px;
}

.utm-parameter {
    display: flex;
    flex-direction: row;
    gap: 8px;
}

.utm-parameter-label {
    width: 167px;
    height: 44px;
    background: #F2F9FE;
    border: 1px solid #F2F9FE;
    border-radius: 5px;
    color: #649BE9;
    display: flex;
    align-items: center;
    padding: 11px 16px;
    justify-content: space-between;
}

.utm-parameter-input {
    width: 420px;
}

/* label {
    margin-bottom: 20px;
} */
label {
    /* margin-top: 10px; */
    display: block;
    text-align: left;
}


input[type="text"] {
    display: block;
    width: 100%;
    height: 42px;
    box-sizing: border-box;
    border-radius: 3px;
    box-shadow: none;
    border: 1px solid #A9A9A9;
    padding: 12px 16px;
}


  input[type="radio"] {
    width: 22px;
    height: 22px;
  }
</style>