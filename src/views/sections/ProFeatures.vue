<template>
  <base-section
    id="pro-features"
  >
    <v-img
      :src="require('@/assets/gidro2.png')"
      class="mx-auto mb-8"
      max-width="128"
    />

    <base-section-heading title="ООО Гидромашина">
      ООО <strong>Гидромашина</strong> проектирует и <br>производит гидравлическое оборудование.
    </base-section-heading>

    <v-container>
      <v-row
        align="center"
        justify="center"
      >
        <v-col
          cols="12"
          md="7"
        >
          <v-simple-table>
            <thead>
              <tr>
                <th />
                <th class="body-1 font-weight-bold text-center">
                  Технические характеристики гидроборта B-HL.A.500
                </th>
                <th class="body-1 font-weight-bold text-center">
                  Технические характеристики гидроборта B-HL.S.500
                </th>
              </tr>
            </thead>

            <tbody class="body-1">
              <tr
                v-for="([name, one, two], i) in features"
                :key="i"
              >
                <td v-text="name" />

                <td class="text-center font-weight-bold">
                  <template v-if="typeof one === 'boolean'">
                    <v-icon :color="one ? 'success' : 'error'">
                      mdi-{{ one ? 'check' : 'close' }}
                    </v-icon>
                  </template>

                  <template v-else>
                    {{ one }}
                  </template>
                </td>

                <td class="text-center font-weight-bold">
                  <template v-if="typeof two === 'boolean'">
                    <v-icon :color="two ? 'success' : 'error'">
                      mdi-{{ two ? 'check' : 'close' }}
                    </v-icon>
                  </template>

                  <template v-else>
                    {{ two }}
                  </template>
                </td>
              </tr>
            </tbody>
          </v-simple-table>
        </v-col>

        <v-col
          cols="12"
          md="5"
        >
          <div class="text-center">
            <base-btn
              :tile="false"
              color="primary"
              href="https://gulyasmir.ru"
              rounded
            >
              Заказать консультацию

              <v-icon right>
                mdi-rocket
              </v-icon>
            </base-btn>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionProChart',

    data: () => ({
      features: [
        ['Грузоподъемность', 23, '40+'],
        ['Высота погрузки', 3, 10],
        ['Регулируемая нагрузка', true, true],
        ['Регулируемая платформа', true, true],
        ['Аккумулятор', false, true],
        ['6 месяцев гарантии', false, true],
        ['Цена', '2000', '5000'],
      ],
    }),
  }
</script>
