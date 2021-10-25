RPGMain.java
public class RPGMain {

        private Braver braver;
        private Monster[] monster;
        public static void main(String[] args){
            RPGMain rpg = new RPGMain();
            //ゲームスタート
            rpg.game();

        }
        public void game(){
            //タイトル表示
            dispTitle();
            //名前入力
            Scanner sc = new Scanner(System.in);
            System.out.println("あなたの名前を入力してください");
            String name = sc.nextLine();
            braver = new Braver(name);

            dispBattleStart();
        }
    }
}

Braver.java
public class Braver extends Creature {
    private final static int MAX_HP = 100;
    private final static int RECOVERY_POINT = 20;
    private final static int CRITICAL_HIT_RATE = 10;

    public Braver(String name){
        super(name,MAX_HP);
    }

    public Creature(String name,int hp){
        this.name = name;
        this.hp = hp;

    }
}

Monster.java
public class Monsters {
    public void dispMonsters(){
        Random r = new Random();
        monsters = new Monster[Monster_NUM];
        for(int i=0; i < Monster_NUM; i++){
            //乱数を取得
            int value = r.nextInt(3);
            if( value == 0){
                monsters[i] = new Slime();
            } else if( value == 1){
                monster[i] = new Wizard();
            }else{
                monsters[i] = new MetalSlime();
    }
    
}
