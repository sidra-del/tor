public class RemoveComments {
    public static void main(String[] args) {
        String code = "int a = 0; // this is a comment\n"
                    + "/* multi-line\n comment */\n"
                    + "a++;";

        // Regex to remove both single-line and multi-line comments
        String cleanedCode = code.replaceAll("//.*|/\\*(.|\\R)*?\\*/", "");

        System.out.println("Code without comments:\n" + cleanedCode);
    }
}
