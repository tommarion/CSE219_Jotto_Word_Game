/*
 * To change this template, choose Tools | Templates
 * and open the template in the editor.
 */
package jotto.game;

import jotto.Jotto;
import properties_manager.PropertiesManager;

/**
 *
 * @author tomma_000
 */
public class InvalidGuessException extends Exception
{
    // THIS WILL STORE INFORMATION ABOUT THE ILLEGAL
    // WORD THAT CAUSED THIS EXCEPTION
    private String invalidGuessWord;

    /**
     * This constructor will keep the illegal word information
     * so that whoever catches this exception may use it in
     * providing informative feedback.
     * 
     * @param initDuplicateGuessWord The illegal word that 
     * caused the exception.
     */
    public InvalidGuessException(String initInvalidGuessWord)
    {
        // STORE THE ILLEGAL WORD SO THAT WE MAY
        // PROVIDE FEEDBACK IF WE WISH
        invalidGuessWord = initInvalidGuessWord;
    }
    
    /**
     * This method returns a textual summary of this exception.
     * 
     * @return A textual summary of this exception, which can
     * be used to provide feedback.
     */
    @Override
    public String toString()
    {
        PropertiesManager props = PropertiesManager.getPropertiesManager();
        String illegalWordFeedback = props.getProperty(Jotto.JottoPropertyType.INVALID_GUESS_ERROR_TEXT);
        return invalidGuessWord + illegalWordFeedback;
    }
}
