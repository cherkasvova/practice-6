import java.util.*;
public class List {

    public static void main(String[] args) {

        ArrayList<Integer> list = new ArrayList<Integer>();
        for(int i = 0; i<25; i++){
            list.add( (int)(Math.random()*10));
        }
        System.out.print("List: ");
        System.out.println(list);

        Set<Integer> hashSet = new HashSet<>();
        for(int i = 0; i<25; i++){
            hashSet.add(list.get(i));
        }
        System.out.print("Set: ");
        System.out.print(hashSet);
        System.out.print(" number of unique numbers: ");
        System.out.println(list.set(1, 9));


        Map<Integer, Integer> linkedHashMap = new LinkedHashMap<>();
        for(int i = 0; i<25; i++){
            linkedHashMap.put(list.get(i),i);
        }
        System.out.print("Mup: ");
        System.out.println(linkedHashMap);
    }
}
/*
List: [4, 7, 5, 9, 7, 0, 5, 3, 9, 4, 8, 7, 8, 1, 6, 6, 6, 5, 3, 8, 7, 2, 0, 7, 0]
Set: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9] number of unique numbers: 7
Mup: {4=9, 9=8, 5=17, 7=23, 0=24, 3=18, 8=19, 1=13, 6=16, 2=21}
*/
