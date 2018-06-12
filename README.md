# addLineNumber
add line number at each line
import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.io.FileWriter;
import java.io.IOException;
import java.io.LineNumberReader;
import java.util.Properties;

public class addNumber {
	public static void main(String[] args) throws IOException {
		LineNumberReader ln=new LineNumberReader(new FileReader("d:\\add.txt"));
		BufferedWriter bw=new BufferedWriter(new FileWriter("d:\\a.txt"));
		String line=null;
		String newLine=null;
		while((line=ln.readLine())!=null) {
			Integer i=Integer.valueOf(ln.getLineNumber());
			newLine=i.toString().concat(line);
			bw.write(newLine);
			bw.newLine();
		}
		ln.close();
		bw.close();
	}
}
