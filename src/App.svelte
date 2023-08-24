<script>
  import {Flex, Container, Button, Image, Center, Divider, Space, Box, Accordion, TextInput, Affix} from "@svelteuidev/core";
  import { fade } from 'svelte/transition';
  import Typewriter from 'svelte-typewriter'
  import MediaQuery from "./MediaQuery.svelte";
	import { ArrowUp } from 'radix-icons-svelte';
  import { fly } from 'svelte/transition';
</script>

<main>
  <MediaQuery query="(max-width: 720px)" let:matches>
    <Flex direction="column" gap="xl">
      <Box css={{
        backgroundColor: "#012C4A",
        color: "white",
        borderRadius: "1rem",
        padding: "3rem",
      }}>
      
        <Flex direction={matches ? "column" : "row"}>
          <Box css={{}}>
            <Image src="logo.png" width={96} height={96} radius="md" />
            <h1 class="app-name-text">Rüya Taşı</h1>
            <h2 class="app-description-text">Rüyalarınız ne anlama geldiğini anında yapay zekadan öğrenin!</h2>
            <p class="app-details-text">Rüya Taşı, rüyalarınızı anlamlandıran ve size rehberlik eden bir uygulamadır. Rüya Taşı, rüyalarınızda karşılaştığınız her şeyi yapay zeka ile çözümler ve size rüyalarınızın ne söylediğini anlatır. Rüya Taşı, rüyalarınızı daha iyi yorumlayabilmeniz ve hayatınıza uygulayabilmeniz için size tavsiyeler ve öneriler verir. Rüya Taşı, rahatlamak istediğinizde huzurlu doğa sesleri dinleyerek kendinizi dinlendirebilir ve daha kaliteli bir uyku çekebilirsiniz. Rüya Taşı ile rüyalarınızın sizi nereye götüreceğini keşfedin!</p>
            <Button color="cyan" radius="xl" size=xl href="https://apps.apple.com/tr/app/r%C3%BCya-ta%C5%9F%C4%B1/id6450684043">
              <Flex gap=sm>
                İndir
                <i class="fa-solid fa-arrow-down"></i>
              </Flex>
            </Button>
          </Box>
          <Center>
            <div class="banner-image">
                <Image src="banner.png" radius="md" />
            </div>
              
          </Center>
        </Flex>
      </Box>
  
      <div class="images" style={!matches && "padding: 2rem"}>
        <Box css={{
          backgroundColor: "#F3F3F3",
          borderRadius: "1rem",
          padding: "2rem",
          textAlign: "left",
        }}>
          <Flex gap=md direction={matches ? "column" : "row"}>
            <Image src="image1.png" radius="md" />
            <Space  w=xl />
            <Image src="image2.png" radius="md" />
            <Space  w=xl />
            <Image src="image3.png" radius="md" />
            <Space  w=xl />
            <Image src="image4.png" radius="md" />
          </Flex>
        </Box>
      </div>

      <div class="faq-area" style={!matches && "padding: 2rem"}>
        <Box css={{
          backgroundColor: "#F3F3F3",
          borderRadius: "1rem",
          padding: "2rem",
          textAlign: "left",
        }}>
          <Accordion radius="lg" variant="separated" chevronPosition="left">
            <h2 class="faq-title">Sıkça Sorulan Sorular</h2>
            <Accordion.Item value="howitworks">
              <div slot="control">Histopia uygulaması nasıl çalışır?</div>
              Histopia, yapay zeka teknolojisi kullanarak tarihi şahsiyetlerle etkileşim kurmanızı sağlar. Kullanıcılar, uygulama aracılığıyla bu figürlerle gerçek zamanlı sohbet edebilir.
            </Accordion.Item>
            <Accordion.Item value="whichfiguresavailable">
              <div slot="control">Hangi tarihi figürlerle konuşabilirim?</div>
              Uygulama geniş bir veritabanına sahip ve tarihi dönemlerden birçok ünlü kişiyle etkileşim kurma fırsatı sunar. Bilim insanlarından sanatçılara, liderlerden düşünürlere kadar birçok isimle sohbet edebilirsiniz.
            </Accordion.Item>
            <Accordion.Item value="isitsecure">
              <div slot="control">Histopia'nın içeriği ne kadar güvenilir?</div>
              Uygulamanın içeriği, tarihi belgelere ve kaynaklara dayanarak hazırlanır. Doğruluk ve güvenilirlik önceliğimizdir, böylece kullanıcılar gerçekçi ve sağlam bilgilerle etkileşim kurabilirler.
            </Accordion.Item>
            <Accordion.Item value="availableon">
              <div slot="control">Uygulamayı hangi cihazlarda kullanabilirim?</div>
              Histopia, Apple App Store'da bulunan bir mobil uygulamadır ve iPhone' da çalışır.             
            </Accordion.Item>
            <Accordion.Item value="properties">
              <div slot="control">Histopia'nın özellikleri nelerdir?</div>
              Histopia, yapay zeka tabanlı canlı sohbetler, geçmişe yolculuk, tarihi figürlerin düşüncelerini anlama gibi özellikler sunar. Akıllı algoritmalar, tarihi kişilikleri canlandırarak etkileşiminizi daha gerçekçi hale getirir.
            </Accordion.Item>
          </Accordion>
        </Box>
      </div>

      <div class="contact-area">
        <Box css={{
          backgroundColor: "rgba(0, 0, 0, 0.87);",
          borderRadius: "1rem",
          padding: "2rem",
          textAlign: "left",
          color: "#f5f5f7",
        }}>
          <h2 style="margin-bottom: 3rem; padding-top: 0rem; margin-top: 0rem;">Bize Ulaşın</h2>
          <div class="content">
            <div class="address-area">
              <h3>İletişim Adreslerimiz</h3>
              <Flex gap=sm direction={matches ? "column" : "row"} justify="space-evenly">
                <div>
                  <h4 class="address-title">Londra</h4>
                  <p>71-75 Shelton Street, Covent Garden, London, United Kingdom, WC2H 9JQ</p>
                </div>
                <div>
                  <h4 class="address-title">İstanbul</h4>
                  <p>Fenerbahçe, Iğrıp Sk. No:13, 34726 Kadıköy/İstanbul</p>
                </div>
  
              </Flex>
            </div>
  
  
            <div class="webpage-area">
              <h3>Web Sayfamız</h3>
              <a href="expozy.co">expozy.co</a>
            </div>
  
            <div class="contactmail-area">
              <h3>E-posta Adresimiz</h3>
              <a href="mailto:hello@hisyopia.app">hello@hisyopia.app</a>
            </div>
          </div>


        </Box>
      </div>
  
    </Flex>

  </MediaQuery>
</main>

<style>
  .content {
    text-align: center;
  }
  .faq-title {
    margin-bottom: 3rem;
    text-align: left;
    padding-top: 0rem;
    margin-top: 0rem;
  }
  
  .app-name-text {
    display: block;
    font-size: 3rem;
    font-weight: 700;
    margin-bottom: 0.5rem;
    text-align: left;
  }

  .app-description-text {
    font-size: 1.5rem;
    font-weight: 400;
    margin-bottom: 3rem;
    text-align: left;
  }

  .app-details-text {
    padding-right: 10rem;
    font-size: 1rem;
    font-weight: 400;
    margin-bottom: 4rem;
    text-align: left;
  }

  .address-title {
    text-align: center;
  }


  @media screen and (max-width: 720px) {
    .app-details-text {
      padding-right: 0rem;
      text-align: center;
    }

    .app-description-text {
      text-align: center;
    }

    .app-name-text {
      text-align: center;
    }

    .banner-image {
      margin-top: 2rem;
    }
  }
</style>
