<template>
    <div class="container">
        <div class="header">
            <h1 class="header-title">Dramaboo</h1>
            <h3 class="header-subtitle">The best drama information webpage for you</h3>
        </div>
        <div class="drama" v-for="(data, index) in drama" :value="data" :key="index">
            <div class="drama-item" v-if="dramaId == data.id">
                <h1 class="page-title">Drama Details</h1>
                <img v-bind:src="data.image"  class="img-fluid img-drama" v-bind:alt="data">
                <div>
                    <h1>{{data.title}}</h1>
                    <h2>Rating : {{data.rating}}</h2>
                    <h4>{{data.release}} | {{data.duration}} | {{data.episode}} | {{data.genre}} | {{data.age}} </h4>
                    <br/><br/>
                    <p>Director : {{data.director}}</p>
                    <p>Cast by : {{data.cast}}</p>
                    <h4>SYNOPSYS</h4>
                    <p class="desc">{{data.desc}}</p>
                </div>
            </div>
        </div>
        <div class="back">
            <router-link to='/'><button class="btn-back">BACK TO HOME</button></router-link>
        </div>
        <div class="footer">
            <h5>Copyright &copy;2020. Created by Rifqi Ardhian. All rights reserved</h5>
        </div>
    </div>
</template>
<script>
import Img1 from '../assets/Drama/at18.jpg';
import Img2 from '../assets/Drama/cly.jpg';
import Img3 from '../assets/Drama/drkim.jpg';
import Img4 from '../assets/Drama/hotel del luna.jpg';
import Img5 from '../assets/Drama/itaewon.jpg';
import Img6 from '../assets/Drama/love alarm.jpg';
import Img7 from '../assets/Drama/ruler.jpg';
import Img8 from '../assets/Drama/vagabond.jpg';


export default {
  data() {
    return {
      dramaId: this.$route.params.id,
      drama: [
        {
          id: 1,
          image: Img1,
          title: 'Moment at Eighteen (2019)',
          rating: '8,3/10',
          release: 'Jul 22, 2019',
          duration: '1 hr 10 min',
          episode: '16 Ep',
          genre: 'Drama, Life, School, Youth',
          age: '15+',
          director: 'Shim Na Yeon',
          cast: 'Ong Sung Woo, Kim Hyang Gi, Shin Seung Ho, Kang Ki Young, and many more.',
          desc: 'Transfer student Jun Woo has no interest in school life, as he is traumatized from being expelled from bullying. Class president Hui Yeong greets Jun Woo warmly on his first day of school. Jun Woo rejects Hui Yeong’s kindness as Hui Yeong’s popularity and influence intimidate him. When an incident breaks out, Jun Woo is falsely accused of stealing a watch. Everyone thinks Jun Woo is the culprit, and Hui Yeong uses his influence among his peers to fuel this rumor. Meanwhile, Soo Bin has been watching Jun Woo all this time. She sees a different side to Jun Woo than the one that other people see, as she notices his cute, goofy streak and innocent smile. Everyone knows that Hui Yeong has a crush on her, but it’s the quiet and attentive Jun Woo that Soo Bin finds herself gravitating towards. Soo Bin’s warmth opens up the softest part of Jun Woo’s heart, and he decides to break out of his shell.',
        },
        {
          id: 2,
          image: Img2,
          title: 'Crash Landing on You (2019)',
          rating: '9,1/10',
          release: 'Dec 14, 2019',
          duration: '1 hr 25 min',
          episode: '16 Ep',
          genre: ' Comedy, Romance, Political',
          age: '15+',
          director: ' Lee Jung Hyo',
          cast: 'Hyun Bin, Son Ye Jin, Seo Ji Hye, Kim Jung Hyun, and many more.',
          desc: 'Tells the story of two star crossed lovers, a South Korean heiress and a North Korean elite who also happens to be an army officer. One day, while paragliding, Yoon Se Ri has an accident caused by strong winds, leading her to crash land in North Korea, where she meets Ri Jung Hyuk, a North Korean army officer, who agrees to help her return to South Korea. Over time, they fall in love, despite the divide and dispute between their respective countries.',
        },
        {
          id: 3,
          image: Img3,
          title: 'Romantic Doctor, Teacher Kim 2 (2020)',
          rating: '8,8/10',
          release: 'Jan 6, 2020',
          duration: '1 hr 10 min',
          episode: '16 Ep',
          genre: 'Romance, Medical',
          age: '15+',
          director: 'Yoo In Shik',
          cast: 'Han Seok Kyu, Ahn Hyo Seop, Lee Sung Kyung, and many more.',
          desc: '“Romantic Doctor Kim” is a “real doctor” story set in a small, humble hospital called Doldam Hospital. It is a story about people who meet Kim Sa Bu, a genius doctor, and discover “real romance.”Kim Sa Bu once gained fame as a top surgeon at a huge hospital. One day, he disappeared from the eyes of the public, quietly becoming the chief surgeon at Doldam Hospital in the countryside. After he conducted a successful operation on Chairman Shin, he gets to improve the hospital under reliable support. But then Chairman Shin passes away, and an old foe returns. New people appear and his students had to leave the hospital. Furthermore, his wrist, which was injured three years ago, starts to act weird. Kim Sa Bu decides to go to a huge hospital himself to solve the manpower shortage at Doldam, where he finds two people who resemble his former students but who seem much more lacking. Seo Woo Jin would do anything for money, and Cha Eun Jae gets nauseous every time she tries to perform surgery. Will Kim Sa Bu be able to run Doldam Hospital with these two?',
        },
        {
          id: 4,
          image: Img4,
          title: 'Hotel del Luna (2019)',
          rating: '8,8/10',
          release: 'Jul 13, 2019',
          duration: '1 hr 20 min',
          episode: '16 Ep',
          genre: 'Mystery, Horror, Comedy, Fantasy, Supernatural',
          age: '15+',
          director: ' Oh Choong Hwan',
          cast: 'IU, Yeo Jin Goo, Jung Dong Hwan, Shin Jung Geun, and many more.',
          desc: 'Jang Man Wol is the CEO of Hotel del Luna. The hotel is situated in downtown in Seoul and has a very old appearance. She made a big error many years ago and, because of this, she has been stuck at Hotel del Luna. She is beautiful, but she is fickle, suspicious and greedy.Goo Chan Sung worked as the youngest assistant manager ever at a multinational hotel corporation. He is a sincere perfectionist. He looks level-headed, but he actually has a soft disposition. Due to an unexpected case, he begins to work as a manager at Hotel del Luna. The hotel`s clientele consists of ghosts.',
        },
        {
          id: 5,
          image: Img5,
          title: 'Itaewon Class (2020)',
          rating: '7,9/10',
          release: 'Jan 31, 2020',
          duration: '1 hr 10 min',
          episode: '16 Ep',
          genre: ' Friendship, Business, Romance, Life, Youth',
          age: '15+',
          director: ' Kim Seong Yoon',
          cast: 'Park Seo Joon, Kim Da Mi, Nara, Yoo Jae Myung, and many more.',
          desc: 'On the first day of attending his new high school, Park Sae Ro Yi punches his classmate Jang Geun Won, who was bullying another classmate. The bully is the son of CEO Jang Dae Hee. The bully`s father runs restaurant business Jagga where Park Sae Ro Yi’s own father works. CEO Jang Dae Hee demands to Park Sae Ro Yi that he apologizes to his son, but Park Sae Ro Yi refuses. Because of his refusal, Park Sae Ro Yi gets expelled from school and his father gets fired from his job. Soon, an accident takes place. Park Sae Ro Yi’s father dies in a motorcycle accident caused by his ex-classmate Jang Geun Won. Burning with anger, Park Sae Ro Yi viciously beats Jang Geun Won. He is soon arrested and receives prison time for violent assault. Park Sae Ro Yi decides to destroy the Jagga company and take revenge upon CEO Jang Dae Hee and his son Jang Geun Won. Once Park Sae Ro Yi is released from prison, he opens a restaurant in Itaewon, Seoul. Jo Yi Seo, who is popular on social media, joins Park Sae Ro Yi’s restaurant and works there as a manager. She has feelings for Park Sae Ro Yi.',
        },
        {
          id: 6,
          image: Img6,
          title: 'Love Alarm (2019)',
          rating: '8,0/10',
          release: 'Aug 22, 2019',
          duration: '50 min',
          episode: '8 Ep',
          genre: 'Friendship, Comedy, Romance, School, Youth',
          age: '13+',
          director: ' Lee Na Jung',
          cast: 'Kim So Hyun, Jung Ga Ram, Song Kang, and many more.',
          desc: 'Cellphone app Joalarm is created. If someone likes you and they are within 10 meters of you, the alarm for the app rings. The app also shows how many people like you, but the app doesn`t reveal specific details on who likes you. Kim Jo Jo is a high school student. She is pretty and smart. She seems like a cheerful person, but her parents died when she was young. Since the death of her parents, Kim Jo Jo has lived with aunt`s family. Living there is not easy for Kim Jo Jo. She doesn`t download the app Joalarm as her phone isn’t new enough. Meanwhile, Hwang Sun Oh is a popular male student at the same high school where Kim Jo Jo attends. He is the son of a wealthy family, but he is not loved by his parents. His best friend Lee Hee Yeong also attends the same high school. Hwang Sun Oh notices that his best friend Lee Hye Yeong likes Kim Jo Jo. Hwang Sun Oh wants to know if his friend really likes her, so he kisses her.',
        },
        {
          id: 7,
          image: Img7,
          title: 'The Emperor: Owner of the Mask (2017)',
          rating: '8,1/10',
          release: ' May 10, 2017',
          duration: '30 min',
          episode: '40 Ep',
          genre: ' Historical, Romance, Drama, Melodrama, Political',
          age: '15+',
          director: ' Park Won Gook, Noh Do Cheol',
          cast: 'Yoo Seung Ho, Kim So Hyun, Kim Myung Soo, and many more.',
          desc: 'As a fictional period drama, this miniseries tells the story of a crown prince named Lee Sun who fights the Pyeonsuhwe society that holds absolute power over the kingdom and also controls the water supply by privatizing it. The drama involves romance, action and court politics as the Crown prince, Lee Sun fights heroically on behalf of the people and Han Ga Eun finds herself falling in love with him instead of avenging the execution of her father at his hands. In “The Emperor: Owner of the Mask,” there is palace intrigue revolving around the true power behind the throne, and a plot twist when the prince switches identities with a commoner. But the overall theme of the show is love, which underlies the romance between a prince and his girl as well as the compassion for the country and people.',
        },
        {
          id: 8,
          image: Img8,
          title: 'Vagabond (2019)',
          rating: '8.5/10',
          release: 'Sep 20, 2019 ',
          duration: '1 hr 10 min',
          episode: '16 Ep',
          genre: 'Action, Thriller, Crime, Melodrama, Investigation',
          age: '15+',
          director: ' Yoo In Shik',
          cast: 'Lee Seung Gi, Bae Suzy, Shin Sung Rok, and many more.',
          desc: 'Cha Dal Gun becomes an awakened tiger in the face of his nephew’s death in a mysterious plane crash. As an orphan himself, he had raised his nephew singlehandedly in place of his brother who had passed on. Triggered by the large-scale cover-up of the incident, he sets off on a journey to discover the truth. Go Hae Ri is the eldest daughter of a marine who had died during an operation. She has always wanted to be a normal civil servant to support her family, but life had other plans and she ends up as a National Intelligence Service (NIS) agent. Their lives intertwine as they discover a tangled web of corruption behind the plane crash. ',
        },
      ],
    };
  },
};
</script>
<style scoped>
    .container {
        width: auto;
    }
    .header {
        padding: 50px;
        grid-column: 1/5;
        background-color: #03a187;
        color: #fff;
        text-align: left;
    }
    .header-title {
      font-family: monospace;
      font-size: 70px;
      color: #deda9e;
    }
    .header-subtitle {
      font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
      font-size: 20px;
    }
    .drama-item {
        padding: 50px;
        width: auto;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-auto-rows: minmax(50px, auto);
        text-align: left;
        background-color: #ededed;
    }
    .page-title {
        grid-column: 1/3;
        text-align: center;
        padding-bottom: 30px;
        background-color: #ededed;
        color: #00c0a0;
        font-family: 'Times New Roman', Times, serif;
    }
    .back {
      text-align: center;
      padding-bottom: 50px;
      background-color: #ededed;
    }
    .btn-back {
        background-color: #00c0a0;
        color: #fff;
        border: 0px;
        border-radius: 60px;
        text-align: center;
        margin: 5px 2px;
        padding: 20px 15px;
        cursor: pointer;
        transition: 0.3s;
        margin: 20px;
        width: 300px;
    }
    .btn-back:hover {
        background-color: transparent;
        border: 2px solid #cfc20e;
        color: #cfc20e;
    }
    .img-drama {
        width: 500px;
        box-shadow: 0 20px 25px 0 rgba(0,0,0,0.2);
        transition: 0.3s ease;
    }
    .desc {
        text-align: justify;
    }
    .footer {
        padding: 10px;
        grid-column: 1/5;
        background-color: #003d3f;
        color: #fff;
        text-align: center;
    }
</style>
