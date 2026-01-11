# Resume_Builder
//Built a Resume Builder application enabling users to enter, store, and fetch resume details in a structured format.
import java.util.Scanner;

public class SmartResumeBuilder {
    static String name, profile, education;
    static String knownLang, progLang, webTech, tools;
    static String experience, projects, contact;
    static boolean resumeCreated = false;
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int choice;
        do {
     System.out.println("\n==============================");
    System.out.println("     IKAAA RESUME BUILDE CHEDAMAA");
    System.out.println("==============================");
    System.out.println("1. Create Resume");
    System.out.println("2. View Resume");
     System.out.println("3. Exit");
     System.out.print("Enter your choice: ");
    choice = sc.nextInt();
     sc.nextLine();
   switch (choice) {
     case 1:
        createResume();
        break;
    case 2:
    viewResume();
     break;
     case 3:
     System.out.println("Thank you! Keep building mannn");
     break;
     default:
    System.out.println("Invalid choice. Try again!");
            }
        } while (choice != 3);
        sc.close();
    }
    static void createResume() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter your name: ");
        name = sc.nextLine();
        System.out.print("Enter your education: ");
        education = sc.nextLine();
        System.out.print("Enter known languages: ");
        knownLang = sc.nextLine();
        System.out.print("Enter programming languages: ");
        progLang = sc.nextLine();
        System.out.print("Enter web technologies (or none): ");
        webTech = sc.nextLine();
        System.out.print("Enter tools known: ");
        tools = sc.nextLine();
        System.out.print("Enter work experience (or fresher): ");
        experience = sc.nextLine();
        System.out.print("Enter projects: ");
        projects = sc.nextLine();
        System.out.print("Enter contact number: ");
        contact = sc.nextLine();
        if (experience.equalsIgnoreCase("fresher") ||
            experience.equalsIgnoreCase("none")) {
            profile = "Motivated fresher eager to learn and grow in software development.";
        } else {
            profile = "Experienced professional with hands-on development skills.";
        }
        resumeCreated = true;
        System.out.println("\nyooo Resume created successfully!");
    }
    static void viewResume() {
        if (!resumeCreated) {
            System.out.println("\noh shitt No resume found. Please create one first.");
            return;
        }
        System.out.println("\n================================");
        System.out.println("        " + name.toUpperCase());
        System.out.println("================================");
        System.out.println("PROFILE: " + profile);
        System.out.println("EDUCATION: " + education);
        System.out.println("KNOWN LANGUAGES: " + knownLang);
        System.out.println("\nTECHNICAL SKILLS");
        System.out.println("--------------------------------");
        System.out.println("Programming: " + progLang);
        System.out.println("Web: " + webTech);
        System.out.println("Tools: " + tools);
        System.out.println("\nEXPERIENCE: " + experience);
        System.out.println("PROJECTS: " + projects);
        System.out.println("CONTACT: " + contact);
        System.out.println("================================");
    }
}
