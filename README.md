import javafx.application.Application;
import javafx.geometry.Insets;
import javafx.scene.Scene;
import javafx.scene.control.*;
import javafx.scene.layout.GridPane;
import javafx.stage.Stage;

public class Main extends Application {

    @Override
    public void start(Stage primaryStage) {
        primaryStage.setTitle("تسجيل الدخول");

        GridPane grid = new GridPane();
        grid.setPadding(new Insets(10, 10, 10, 10));
        grid.setVgap(8);
        grid.setHgap(10);

        Label nameLabel = new Label("اسم المستخدم:");
        GridPane.setConstraints(nameLabel, 0, 0);

        TextField nameInput = new TextField();
        nameInput.setPromptText("أدخل اسم المستخدم");
        GridPane.setConstraints(nameInput, 1, 0);

        Label passwordLabel = new Label("كلمة المرور:");
        GridPane.setConstraints(passwordLabel, 0, 1);

        PasswordField passwordInput = new PasswordField();
        passwordInput.setPromptText("أدخل كلمة المرور");
        GridPane.setConstraints(passwordInput, 1, 1);

        Button loginButton = new Button("تسجيل الدخول");
        GridPane.setConstraints(loginButton, 1, 2);

        Button registerButton = new Button("إنشاء حساب جديد");
        GridPane.setConstraints(registerButton, 1, 3);

        grid.getChildren().addAll(nameLabel, nameInput, passwordLabel, passwordInput, loginButton, registerButton);

        loginButton.setOnAction(e -> {
            // يتم تنفيذ الكود لتسجيل الدخول هنا
            // يمكنك التحقق من اسم المستخدم وكلمة المرور وتنفيذ الإجراء المناسب
        });

        registerButton.setOnAction(e -> {
            // يتم تنفيذ الكود لإنشاء حساب جديد هنا
            // يمكنك جمع بيانات الحساب الجديد وتخزينها في قاعدة بيانات أو ملف
        });

        Scene scene = new Scene(grid, 300, 200);
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
