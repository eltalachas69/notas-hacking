## Descripción
This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://challenge-files.cylabacademy.net/library/14bca593f597cbc6b521a3deb17bd94a81c603c8cdc801f0a6b41f89ec79e27f/VaultDoor3.java)
## Solución
Para solucionarlo estaba viendo el codigo y vi que ahi mismo nos daba la bandera, al principio pense que esa era la bandera pero no, resulta que teniamos que ordenarlo mediante el metodo que nos daba abajo, entonces lo que hice fue agarrar ese codigo y lo puse en otro codigo, cuando lo estaba haciendo vi que estaba incompleto pero no era otra cosa importante, solo era ponerle los datos de la i pero nada complicado ya que ahi mismo nos decia en el limite, por ejemplo en uno llegaba hasta que fuera menor de  8 entonces en el siguiente donde empezaba pues era el 8 y asi, entonces pues me dio la bandera que es `academy{jU5t_a_s1mpl3_an4gr4m_4_u_2be258}`

Codigo vault:
```
 public static void main(String args[]) {
        VaultDoor3 vaultDoor = new VaultDoor3();
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
	String input = userInput.substring("academy{".length(),userInput.length()-1);
	if (vaultDoor.checkPassword(input)) {
	    System.out.println("Access granted.");
	} else {
	    System.out.println("Access denied!");
        }
    }

    // Our security monitoring team has noticed some intrusions on some of the
    // less secure doors. Dr. Evil has asked me specifically to build a stronger
    // vault door to protect his Doomsday plans. I just *know* this door will
    // keep all of those nosy agents out of our business. Mwa ha!
    //
    // -Minion #2671
    public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
        char[] buffer = new char[32];
        int i;
        for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        }
        String s = new String(buffer);
        return s.equals("jU5t_a_sna_3lpm15ge42_u_4_mbr248");
    }
}
```

Codigo que hice:
```
public class holaesteesmiprogramaenjavajejejeje{
public static void main(String[] holaestoesparacorrerlojejeje){
String testo = "jU5t_a_sna_3lpm15ge42_u_4_mbr248";
char[] buffer = new char[32];
        int i;
        for (i=0; i<8; i++) {
            buffer[i] = testo.charAt(i);
        }
        for (i=8; i<16; i++) {
            buffer[i] = testo.charAt(23-i);
        }
        for (i=16; i<32; i+=2) {
            buffer[i] = testo.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = testo.charAt(i);
        }
        String contrasenia = new String(buffer);
        System.out.println(contrasenia);
}
}

```

Terminal
```
┌──(kali㉿kali)-[~/Projects/picoCTF/Reversing/vaultdoor3]
└─$ javac holaesteesmiprogramaenjavajejejeje.java 
holaesteesmiprogramaenjavajejejeje.java:18: error: variable testo is already defined in method main(String[])
        String testo = new String(buffer);
               ^
1 error
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/Reversing/vaultdoor3]
└─$ javac holaesteesmiprogramaenjavajejejeje.java 
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/Reversing/vaultdoor3]
└─$ java VaultDoor3                              
Enter vault password: ^C                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/Reversing/vaultdoor3]
└─$ java holaesteesmiprogramaenjavajejejeje      
jU5t_a_s1mpl3_an4gr4m_4_u_2be258

```
## Notas Adicionales 
## Referencias
