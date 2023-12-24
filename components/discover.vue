<template>
  <!-- creates the card element for the page -->
  <v-card class='main-bg text-black'>
    <!-- page title  -->
    <v-card-title class='text-center mb-8'>
      High Karat Gold:
      <br>
      The Complete Guide to Understanding Gold Quality
      <br>
      (Content credit: ©2023 Brilliant Earth, LLC)
    </v-card-title>

    <!-- first image of the page -->
    <v-img :src='images.img1' class='about-images disco-img' />

    <!-- creates a grid -->
    <v-row>
      <!-- column for the grid -->
      <v-col cols='10' offset='1'>
        <!-- item one of the column -->
        <v-card-item>
          Firstly, let’s settle it: Karat or Carat? Carat with a C refers to the carat weight – 
          or size – of a diamond or gemstone. Karat with a K, on the other hand, refers to the 
          purity of gold a jewelry design is crafted with. Karat with a K is what we’ll be 
          discussing today.
        </v-card-item>
        <!-- item two of the column -->
        <v-card-item>
          Gold is undoubtedly one of the most valuable metals on the planet. Its high malleability 
          and resistance to corrosion make it an excellent choice for jewelry because it can be 
          hammered and shaped into different designs while maintaining its integrity. Read on to 
          learn more about gold and its various purity levels.
        </v-card-item>
      </v-col>
    </v-row>

    <!-- second image of the page -->
    <v-img :src='images.img2' class='about-images disco-img' />

    <!-- creates grid -->
    <v-row>
      <!-- column for the grid -->
      <v-col cols='10' offset='1'>
        <!-- creates grid item in the column -->
        <v-card-item>
          <!-- creates terms to know list -->
          <v-list lines='two' class='main-bg text-black'>
            <h2 class='pl-4'>Gold Terms to Know</h2>
            <!-- shows the items in terms list -->
            <v-list-item v-for='term in terms'>
              <strong>{{ term.title }}</strong>{{ term.content }}
            </v-list-item>
          </v-list>
        </v-card-item>
      </v-col>
    </v-row>

    <!-- third image of the page -->
    <v-img :src='images.img3' class='about-images disco-img' />

    <!-- creates grid for the content -->
    <v-row class='pt-6 pb-6'>
      <!-- column for the grid -->
      <v-col cols='10' offset='1'>
        <!-- first item in the column -->
        <v-card-item title='What Is A Karat?'>
          Karat is defined as a measurement of the purity of gold. 24 karat (24K) gold is pure 
          gold alloyed with no other metals. 18 karat (18K) gold is crafted with 75% pure gold 
          and 25% other alloys. 14 karat (14K) gold is crafted with 58.3% pure gold and 41.7% 
          other alloys. 10 karat (10K) gold is usually the least pure gold on offer for anything 
          considered to be ‘gold jewelry.’ It features 41.7% pure gold and 58.3% other metals.
          <br>
          As a note, these percentages do vary slightly from jeweler to jeweler as they craft 
          the perfectly toned metal that works for them. Anything branded as a particular karat, 
          however, will be very close to the percentages dictated by the millesimal fineness chart.
          <br>
          Another note that’s worth mentioning is skin irritation. Many people can be allergic to 
          the alloys (such as zinc) used in types of gold jewelry which can cause rashes or other 
          skin irritations. So be careful and inquire which alloys were used to create the piece 
          you’re considering purchasing.
        </v-card-item>
        <!-- second item in the column -->
        <v-card-item title='What’s the Difference Between Karat and Carat?'>
          Karat is a measurement of the purity of gold. Metals like 24 karat (24K) and 18 karat (18K) 
          are created with more pure gold than a 10 karat (10K) metal is. Karat is not to be confused 
          with carat, which refers to the weight of a gemstone or diamond.
        </v-card-item>
      </v-col>
    </v-row>

    <!-- fourth image of the page -->
    <v-img :src='images.img4' class='about-images disco-img'/>

    <!-- creates grid for the content -->
    <v-row class='pt-6 pb-6'>
      <!-- column in the grid -->
      <v-col cols='10' offset='1'>
        <!-- items for the column -->
        <v-card-item title='What Is Gold Purity?'>
          Gold purity refers to the percentage of gold in an alloy. There are two ways to measure 
          the purity of gold. The first method involves karat expressed as a number from 1 to 24 
          (with 24 being the highest karat gold). The second method is millesimal fineness, 
          described as parts per thousand.
          <br><br>
          The most common purity measure for gold jewelry is Karat (K), which is measured based 
          on the weight of the gold in an item relative to the importance of all other metals. 
          For example, 18K is 18/24ths pure gold, and 14K is 14/24ths pure gold.
          <br><br>
          Below is the Millesimal Fineness system, which explains the numbers behind karat and 
          gold purity.
        </v-card-item>
      </v-col>
    </v-row>

    <!-- creates grid for the page -->
    <v-row class='pt-6 pb-6'>
      <!-- column in the grid -->
      <v-col cols='10' offset='1'>
        <!-- creates table for the column -->
        <v-table class='main-bg text-black'>
          <!-- table header -->
          <thead>
            <!-- table header row -->
            <tr>
              <!-- dynamically creates the table headers -->
              <th v-for='header in tableHeader'>
                {{ header.header }}
              </th>
            </tr>
          </thead>
          <!-- table body -->
          <tbody>
            <!-- creates the table body rows -->
            <tr v-for="content in tableContent" :key="content">
              <!-- dynamically inserts table body content -->
              <td>{{ content.karats }}</td>
              <td>{{ content.fraction }}</td>
              <td>{{ content.percent }}</td>
              <td>{{ content.mill }}</td>
            </tr>
          </tbody>
        </v-table>
      </v-col>
    </v-row>

    <!-- fifth image of the page -->
    <v-img :src='images.img5' class='about-images disco-img' />

    <!-- creates grid for the page -->
    <v-row class='pt-6 pb-6'>
      <!-- creates column in the grid -->
      <v-col cols='10' offset='1'>
        <!-- first item for the column -->
        <v-card-item title='What Is the Difference Between Pure and High Karat Gold?'>
          The karat is a measure of how much pure gold is used to make each piece of 
          jewelry. Pure or 24-karat gold has 100% pure gold. High karat gold refers 
          to any piece with more than ten karats of pure gold. Typically, you won’t 
          find anything less than 10K gold on market for high end jewelry.
        </v-card-item>
        <!-- second item for the column -->
        <v-card-item title='What Is the Highest Karat of Gold?'>
          The highest karat of gold is 24K gold. 24 karat gold is 100% pure and doesn’t contain 
          any other metals, making it the purest gold available. This means that it has zero 
          impurities and is usually softer than lower karats—10K and 14K.
          <br><br>
          There are many different karat levels of gold. The higher the karat, the fewer other 
          metals added to it during the refining process. 24K use in wedding bands and other 
          jewelry is limited because its softness means that it can’t hold fine details like 
          subtle curves on intricate designs. Thus, 10K gold is the most durable, containing 
          41.7% pure gold. It’s often used in jewelry.
        </v-card-item>
        <!-- third item for the column -->
        <v-card-item title='Does a Higher Karat Mean Higher Quality Gold?'>
          Simply put, no. 24K gold is the highest karat gold, but that doesn’t necessarily 
          mean it is of a higher quality. It does mean that there is more gold in it than 
          there is in 14K or 10K and therefore it’s more valuable, but not necessarily better. 
          24 karat gold is rarely used in jewelry as its very soft. 18 karat gold is the most 
          used for women and men’s rings and fine jewelry designs as it’s as beautiful as it 
          is durable.
        </v-card-item>
      </v-col>
    </v-row>

    <!-- sixth image for the page -->
    <v-img :src='images.img6' class='about-images disco-img' />

    <!-- creates grid -->
    <v-row class='pt-6 pb-6'>
      <!-- column in the grid -->
      <v-col cols='10' offset='1'>
        <!-- first item in the column -->
        <v-card-item title='How Can You Tell if Gold Is Real?'>
          The best way to tell if gold is real is to bring it in to a reputable jeweler who can 
          test it for you.
          <br><br>
          If you’re eager to discover if your gold is real at home, look it over to see if it is 
          stamped. Any real gold should be stamped somewhere with its karat measurement 
          (usually 10K, 14K, or 18K). But remember, a stamp doesn’t fully prove a piece’s 
          authenticity, so it’s always best to test in more ways than one.
          <br><br>
          If you have found a stamp and want to further test if an item is crafted with pure 
          gold, try the water test. Take a bowl or glass, fill it with water, and drop the gold 
          into it. If it floats, it’s surely not real gold. If it sinks to the bottom, there’s a 
          much better chance that what you have is real – true gold is very heavy. Again, the 
          water test doesn’t fully prove authenticity. Ensure you bring it in to your jeweler 
          for a full test before celebrating.
        </v-card-item>
        <!-- second item in the column -->
        <v-card-item title='How to Choose the Best Karat for You'>
          The best karat will depend on what you’re looking for and what the gold will be used for.
          <br><br>
          For items like a ring that you wear on your hands, you’ll want at the very least 18K gold. 
          This is because we so often use our hands, to work, to play, to do chores – it’s quite 
          easy for rings to get scuffed if we’re keeping them on all day. 24K, in this regard, is 
          much too soft. 18K, 14K, and 10K are the best options for everyday use rings.
          <br><br>
          For items like pendants or earrings, it’s not the end of the world for people choose a 
          design that’s crafted in 24K. As these aren’t items worn on your hands and they generally 
          just rest on your body, there’s less of a chance for them to be damaged.
          <br><br>
          There’s also a difference in color when considering yellow gold engagement rings with 
          different gold alloys. 18K yellow gold is often a much more deeply saturated yellow/green 
          color often referred to as ‘buttery’, whereas 14K gold is a much lighter, more subtle hue 
          of gold. So, the one you choose will also have an effect on the look of your piece, not 
          just its durability.
        </v-card-item>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
  // imports for the page
  import img1 from '@/assets/about1.jpg'
  import img2 from '@/assets/about2.jpg'
  import img3 from '@/assets/about3.jpg'
  import img4 from '@/assets/about8.jpg'
  import img5 from '@/assets/about5.jpg'
  import img6 from '@/assets/about6.jpg'

  // exports data
  export default {
    data: () => ({
      // images array
      images: { img1, img2, img3, img4, img5, img6 },
      // terms obj
      terms: [
        {
          title: 'Alloy: ',
          content: 'an alloy is a metal created by mixing two or more metallic elements. Alloys are' +
          ' most often created to strengthen, aid in corrosion-resistance, or alter the color of a'+
          ' metal. For example, combining pure gold with other metals like copper or zinc creates what'+
          ' we know as yellow gold, and adds strength to the metal, making it more durable. White gold is'+
          ' often mixed with nickel and zinc. Rose gold uses a combination of all alloys mentioned above'+
          ' to achieve its distinctive look.'
        },
        {
          title: 'Ductile/Ductility: ',
          content: 'ductile, from the Latin root ‘ductillis,’ refers to malleability – how much can'+
          ' something be stretched while retaining its structural integrity? In terms of gold, ductility'+
          ' refers directly to how much a metal can be deformed or altered without losing its strength.'+
          ' Metals like gold and nickel are extremely ductile and can be stretched into very thin wire.'
        },
        {
          title: 'Gold Purity: ',
          content: 'the purity of gold refers to the percentage of pure gold present. For example,'+
          ' pure gold is mixed with nickel and zinc (and therefore becomes an alloy) to create white'+
          ' gold. A purely gold ring (24 karat, the highest karat gold) could prove to be too ductile'+
          ' for everyday wear.'
        },
        {
          title: 'Hallmark: ',
          content: 'hallmarks refer to the small imprints stamped onto gold jewelry that disclose karat.'+
          ' ‘10K,’ ‘14K,’ or ‘18K’ are often stamped onto the inner edge of an engagement ring or the'+
          ' clasp on a piece of jewelry to call out that the item is created with real gold. Tip: always'+
          ' ensure the gold jewelry that you buy is at the very least stamped with a karat identifier.'+
          ' Company or country-based hallmarks, unique branded symbols, are also often stamped onto high'+
          ' end jewelry designs.'
        },
        {
          title: 'Karat: ',
          content: 'karat refers to the purity of gold. 10 karat gold will have the highest percentage'+
          ' of alloy metals and the lowest percentage of pure gold. 24 karat gold is the highest karat'+
          ' gold and has the lowest percentage of alloy metals and the highest percentage of pure gold.'
        },
        {
          title: 'Malleability: ',
          content: 'malleability refers to a metals capability of being shaped or extended by'+
          ' hammering or forging.'
        },
        {
          title: 'Millesimal Fineness: ',
          content: 'millesimal fineness is a system of denoting the purity of platinum, gold,'+
          ' and silver alloys by parts per thousand of pure metal in the alloy. For example, 50%'+
          ' gold would be noted as 500 on the millesimal fineness scale.'
        }
      ],
      // table headers
      tableHeader: [
        {header: 'Number of Karats'}, 
        {header: 'Fraction of Gold'}, 
        {header:'% of Gold Purity'},
        {header: 'Millesimal, Finesess'}
      ],
      // table content obj
      tableContent: [
        {
          karats: '10k',
          fraction: '10/24',
          percent: '41.7',
          mill: '416/417'
        },
        {
          karats: '12k',
          fraction: '12/24',
          percent: '50.0',
          mill: '500'
        },
        {
          karats: '14k',
          fraction: '14/24',
          percent: '58.3',
          mill: '583/585'
        },
        {
          karats: '18k',
          fraction: '18/24',
          percent: '75.0',
          mill: '750'
        },
        {
          karats: '22k',
          fraction: '22/24',
          percent: '91.7',
          mill: '916/917'
        },
        {
          karats: '24k',
          fraction: '24/24',
          percent: '99.9',
          mill: '999'
        },
      ]
    }),
  }
</script>