<template>
  <div class="container mx-auto px-[24px] pr-[31px] mt-[64px] lg:(px-[128px] mt-[80px])">
    <div class="flex text-[14px] font-medium space-x-[10px] tracking-tighter">
      <div class="text-[#111721]">
        Главная
      </div>
      <img src="@/assets/img/arrow-down.svg" alt="">
      <div class="text-[#b3b3b3]">
        Новости
      </div>
    </div>

    <div class="font-bold text-[22px] leading-[28px] mt-[34px] lg:(text-[48px] leading-[48px])">
      Атлантис-Пак<br> приглашает на IFFA-2019
    </div>

    <div class="hidden lg:block font-medium mt-[34px] text-[14px] leading-[19px] text-[#A6A6A6]">
      29 март / 2019
    </div>

    <div class="font-medium text-[14px] leading-[21px] mt-[22px] tracking-tighter lg:(text-[21px] leading-[32px] mt-[48px])">
      Компания «Атлантис-Пак» примет участие в выставке IFFA-2019, которая будет проходить во Франкфурте-на-Майне с 4 по 9 мая. «Атлантис-Пак» является постоянным участником выставки на протяжении многих лет — это будет уже 8 выставка IFFA для компании.
    </div>
  </div>

  <img class="w-full h-[212px] object-cover mt-[24px] lg:(mt-[43px] h-[576px])" src="@/assets/img/article.jpg" alt="дом с вертолетом">

  <div class="container mx-auto px-[24px] pr-[31px] lg:(px-[128px])">
    <div class="text-[#4D4F51] text-[12px] leading-[18px] mt-[18px] lg:(text-[18px] leading-[32px] mt-[32px] pr-[110px] tracking-tighter)">
      Девиз «Атлантис-Пак» на IFFA-2019 – «Сохранение природы никогда ещё не было таким прибыльным». Акцент на бережном отношении компании к природе не случаен. По сравнению с другими способами производства упаковочных решений, при производстве инновационных плёнок, оболочек и пакетов «Атлантис-Пак»  расходуется значительно меньше водных ресурсов. Плёнки АМИСТАЙЛ имеют очень маленькую толщину (от 30 мкм), но по техническим показателям соответствуют материалам в 1,5-2 раза толще.
    </div>

    <img src="@/assets/img/table-1.jpg" class="mt-[16px] lg:hidden" alt="таблица">

    <table class="article_table mt-[44px] hidden lg:table">
      <thead>
        <tr>
          <th>Значение 1</th>
          <th>Значение 2</th>
          <th>Значение 3</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Adidas</td>
          <td>Table Generator plugin automates</td>
          <td>43</td>
        </tr>
        <tr>
          <td>Puma</td>
          <td>Copy paste the data</td>
          <td>35</td>
        </tr>
        <tr>
          <td>Nike</td>
          <td>For updates to the plugin</td>
          <td>36</td>
        </tr>
        <tr>
          <td>New Balance</td>
          <td>The plugin provides the custom</td>
          <td>33</td>
        </tr>
      </tbody>
    </table>

    <div class="overflow-x-auto pb-[20px] mt-[34px] lg:(overflow-hidden pb-0)">
      <table class="article_table">
        <thead>
          <tr>
            <th>Значение 1</th>
            <th>Значение 2</th>
            <th>Значение 3</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Adidas</td>
            <td>Table Generator plugin automates</td>
            <td>43</td>
          </tr>
          <tr>
            <td>Puma</td>
            <td>Copy paste the data</td>
            <td>35</td>
          </tr>
          <tr>
            <td>Nike</td>
            <td>For updates to the plugin</td>
            <td>36</td>
          </tr>
          <tr>
            <td>New Balance</td>
            <td>The plugin provides the custom</td>
            <td>33</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style scoped>
table.article_table {
  width: 100%;
  min-width: 768px;
  background-color: #ffffff;
  border-collapse: collapse;
  border-width: 1px;
  border-color: #DF1D3B;
  border-style: solid;
  color: #000000;
}

table.article_table td, table.article_table th {
  border-width: 1px;
  border-color: #DF1D3B;
  border-style: solid;
  padding-left: 10px;
  padding-top: 10px;
  padding-bottom: 8px;
  font-size: 14px;
}

table.article_table td {
  border-width: 1px;
  border-color: #DF1D3B;
  border-style: solid;
  padding-left: 10px;
  padding-top: 10px;
  font-weight: 400;
  padding-bottom: 6px;
  font-size: 12px;
}

table.article_table thead {
  background-color: #DF1D3B;
  color: white;
  text-align: left;
}

td:nth-child(1) {
  font-weight: 700 !important;
  font-size: 14px !important;
}

table.article_table thead th {
  padding-left: 10px;
}
</style>
