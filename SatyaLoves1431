import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;

class Result {

    /*
     * Complete the 'sockMerchant' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts following parameters:
     *  1. INTEGER n
     *  2. INTEGER_ARRAY ar
     */

    public static int sockMerchant(int n, List<Integer> ar) {
    // Write your code here
        HashMap<Integer, Integer> hm=new HashMap<>();
        int res=0;
        for(int i=0;i<ar.size();i++)
        {
            if(hm.containsKey(ar.get(i)))
            {
                hm.put(ar.get(i), hm.get(ar.get(i))+1);
            }
            else
            {
                hm.put(ar.get(i), 1);
            }
        }
        Collection<Integer> values = hm.values();
        ArrayList<Integer> listOfValues = new ArrayList<>(values);
        for(int i=0;i<listOfValues.size();i++)
        {
            if(listOfValues.get(i)>1)
            {
                res=(int) Math.floor((listOfValues.get(i))/2)+res;
            }
        }
        return res;

    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int n = Integer.parseInt(bufferedReader.readLine().trim());

        List<Integer> ar = Stream.of(bufferedReader.readLine().replaceAll("\\s+$", "").split(" "))
            .map(Integer::parseInt)
            .collect(toList());

        int result = Result.sockMerchant(n, ar);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}
