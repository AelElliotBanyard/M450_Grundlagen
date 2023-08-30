# Aufgabe 1
## Formen von Tests aus der Informatik
### Unit-Test
Dieser Test untersucht das Verhalten einer einzelnen Komponente.
```java
import static org.junit.jupiter.api.Assertions.assertEquals;
import org.junit.jupiter.api.Test;

public class MathUtilsTest {

    @Test
    public void testAdd() {
        int result = MathUtils.add(3, 5);
        assertEquals(8, result);
    }
}
```
### Integration-Test
Dieser Test untersucht die Interaktion zwischen verschiedenen Komponenten.
```java
import unittest
from database import Database
from app import Application

class AppIntegrationTest(unittest.TestCase):

    def setUp(self):
        self.db = Database()
        self.app = Application(self.db)

    def test_save_data(self):
        data = "Test Data"
        self.app.save(data)
        result = self.db.retrieve()
        self.assertEqual(data, result)

if __name__ == '__main__':
    unittest.main()
```
### Acceptance-Test
Dieser Test überprüft, ob das System die erwarteten Ergebnisse liefert.
```java
describe('Login Test', () => {
  it('should log in successfully', () => {
    cy.visit('/login')
    cy.get('[data-test=username]').type('user123')
    cy.get('[data-test=password]').type('password123')
    cy.get('[data-test=login-button]').click()
    cy.url().should('include', '/dashboard')
    cy.get('[data-test=welcome-message]').should('contain', 'Welcome, user123!')
  })
})
```