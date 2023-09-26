package org.example;
import java.util.Scanner;
import javax.sound.sampled.*;
import java.io.File;

public class Main {
static String strResponse;
public static void main(String[] args) {
new Main();
}
public Main() {
try {
File filename = new File("C:\\Users\\lizam\\Downloads\\onlymp3.to - lana_del_rey___cry_kill_die__unreleased__-0HbvkXS4L-I-192k-1694843511.wav");
AudioInputStream audio = AudioSystem.getAudioInputStream(filename);
Clip clip = AudioSystem.getClip();
clip.open(audio);
Scanner scan = new Scanner(System.in);
System.out.println("Press any key to play the audio:  ");
strResponse = scan.next();
clip.start();
System.out.println("The audio is playing!!");
Thread.sleep(500000);
} catch (Exception e){
e.printStackTrace();
}
}
}